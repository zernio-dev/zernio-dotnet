# Zernio.Api.LinkedInMentionsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetLinkedInMentions**](LinkedInMentionsApi.md#getlinkedinmentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve LinkedIn mention |

<a id="getlinkedinmentions"></a>
# **GetLinkedInMentions**
> GetLinkedInMentions200Response GetLinkedInMentions (string accountId, string url, string? displayName = null)

Resolve LinkedIn mention

Converts a LinkedIn profile or company URL to a URN for @mentions in posts.  You usually do not need this endpoint. Put the profile or company URL inside `@[...]` in the post `content` (for example `@[https://www.linkedin.com/in/vincentjong]`) and the post resolves it for you, using LinkedIn's own name. Use this endpoint to preview what a URL resolves to, or to get ready-made `@[Name](urn)` markup, which still works in `content` and is published exactly as written.  Example: - Resolve: GET /v1/accounts/{id}/linkedin-mentions?url=linkedin.com/in/vincentjong - Returns: mentionFormat: \"@[Vincent Jong](urn:li:person:xxx)\" - Use in post content: \"Great talk with @[Vincent Jong](urn:li:person:xxx) today!\"  Important: The mentions array field in POST /v1/posts is stored for reference only and does NOT trigger @mentions on LinkedIn. Write the mention in the content text.  Requirements: - Resolving a profile URL to a person mention requires the LinkedIn account to be admin of at least one organization: both endpoints that resolve a profile URL to a member URN take an organization you administer. A resolved person mention publishes from any account. Organization mentions (e.g. @Microsoft) have no such requirement. - The two are not scoped alike. peopleTypeahead?q=organizationFollowers only returns that organization's followers; vanityUrl?q=vanityUrlAsOrganization does not, and its resolvable set is opaque. A 404 here does not mean the person is unknown to you or unknown to LinkedIn: a live public profile can 404 with no reason given. - displayName is deprecated and ignored in practice: the endpoint reads the person's real name from LinkedIn itself. LinkedIn renders a person mention as a link only when the mention text is the person's first name, last name or full name (case-sensitive). - Person mentions DO work when published from personal profiles (the URN only needs to be valid). The limitation is only in the resolution step (URL to URN), not in publishing. 

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using Zernio.Api;
using Zernio.Client;
using Zernio.Model;

namespace Example
{
    public class GetLinkedInMentionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://zernio.com/api";
            // Configure Bearer token for authorization: bearerAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new LinkedInMentionsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The LinkedIn account ID
            var url = miquelpalet;  // string | LinkedIn profile URL, company URL, or vanity name.
            var displayName = Miquel Palet;  // string? | Deprecated: omit it. When sent for a person it overrides the mention text, and LinkedIn renders the mention only if it is exactly the person's first name, last name or full name (case-sensitive). When omitted the real name is read from LinkedIn. Ignored for org mentions, which always use the organization's LinkedIn name. (optional) 

            try
            {
                // Resolve LinkedIn mention
                GetLinkedInMentions200Response result = apiInstance.GetLinkedInMentions(accountId, url, displayName);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInMentionsApi.GetLinkedInMentions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLinkedInMentionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resolve LinkedIn mention
    ApiResponse<GetLinkedInMentions200Response> response = apiInstance.GetLinkedInMentionsWithHttpInfo(accountId, url, displayName);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInMentionsApi.GetLinkedInMentionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The LinkedIn account ID |  |
| **url** | **string** | LinkedIn profile URL, company URL, or vanity name. |  |
| **displayName** | **string?** | Deprecated: omit it. When sent for a person it overrides the mention text, and LinkedIn renders the mention only if it is exactly the person&#39;s first name, last name or full name (case-sensitive). When omitted the real name is read from LinkedIn. Ignored for org mentions, which always use the organization&#39;s LinkedIn name. | [optional]  |

### Return type

[**GetLinkedInMentions200Response**](GetLinkedInMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | URN resolved successfully |  -  |
| **400** | Invalid request or no organization found (for person mentions) |  -  |
| **401** | Missing or invalid API key (&#x60;missing_credentials&#x60; or &#x60;invalid_credentials&#x60;), or LinkedIn revoked or expired the account&#39;s token (&#x60;reconnect_required&#x60;, reconnect the account). |  -  |
| **403** | The account holds no organization role that can resolve person mentions |  -  |
| **404** | Account, person or organization not found |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted.  Reddit rate-limits per connected Reddit user (1000 requests per 10-minute window), and that budget is shared by every operation using that account. Retry after the window resets rather than retrying immediately; repeated calls while exhausted do not succeed and keep the budget spent.  Google Ads: writes and reports run on one developer token shared by every Google Ads account on Zernio. The token holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. The envelope has &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed.  YouTube Analytics: reads (channel-insights, demographics, daily-views, video-retention) run on the \&quot;Queries per day\&quot; quota of the Google Cloud project the YouTube account is connected through, shared with other Zernio customers, so a 429 there is not your own volume. It resets at midnight Pacific Time. The envelope has &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed.  Meta ads: every Meta throttle (codes 4, 17, 32, 613 and the business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta itself answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when Meta sends one, otherwise it is Meta&#39;s documented 60-second minimum (30 seconds for the one-write-per-30-seconds limit on a single object).  Pinterest ads: Pinterest rate-limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when it sends one, otherwise 60 seconds.  TikTok ads: TikTok caps requests per second and answers overage with code 40100 or with code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (for example one ad at a time per advertiser) instead of retrying at once. The Smart+ review read (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has a stricter quota of its own on TikTok: after an overage Zernio answers 429 for that advertiser and connection, without calling TikTok, for about 60 seconds, then 120, then 240 while TikTok keeps refusing (one step down after a successful call, each with up to 10% of random jitter); &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;incomplete: true&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

