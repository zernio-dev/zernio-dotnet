# Zernio.Api.AdLibraryApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SearchAdLibrary**](AdLibraryApi.md#searchadlibrary) | **GET** /v1/ads/library | Search the public Ad Library |

<a id="searchadlibrary"></a>
# **SearchAdLibrary**
> SearchAdLibrary200Response SearchAdLibrary (string? platform = null, string? accountId = null, string? q = null, string? pageIds = null, string? advertiser = null, string? countries = null, string? adType = null, string? status = null, string? platforms = null, string? mediaType = null, string? languages = null, DateOnly? since = null, DateOnly? until = null, string? searchType = null, string? fields = null, int? limit = null, string? after = null)

Search the public Ad Library

Searches Meta's or LinkedIn's public Ad Library to see what ads other advertisers run, for competitor and market research.  ### Which library is searched  - Meta's Ad Library (`GET /ads_archive`) is searched with Zernio's own developer access, so `platform=meta` needs no connected account at all. - LinkedIn's Ad Library (`GET /rest/adLibrary`) runs on a connected `linkedin` / `linkedinads` account, passed as `accountId`. - Passing a Meta account as `accountId` also selects Meta.  Rows are returned in the platform's raw shape under `data`. `paging.after` is an opaque cursor on both (`null` when exhausted).  **Meta coverage.** Political and social-issue ads are searchable worldwide. Every other ad is in the archive only if it was delivered to the EU or UK within the last year, so a US-only commercial advertiser is invisible.  Spend, impressions and demographics are political-only fields and are left out of the default projection; request them via `fields`.  **Meta rate limit.** Meta searches are capped at 30 requests per hour per team, because all customers share Zernio's Meta quota. Meta can also throttle that shared quota. Either way you get a `429` with `Retry-After`: wait that long before retrying.  **LinkedIn coverage.** Ads served after June 1 2023, worldwide, kept for a year after their last impression. EU-delivered ads carry impression ranges and the disclosed targeting facets.  Pages are capped at 25 ads (`limit` > 25 is a 400). `after` is the next offset.  ### Which params apply  - Both: `q`, `countries`, `limit`, `after` - Meta-only: `pageIds`, `adType`, `status`, `platforms`, `mediaType`, `languages`, `searchType`, `fields`, `since`, `until` - LinkedIn-only: `advertiser`  Passing a param the account's platform does not support is a 400 naming the param. 

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
    public class SearchAdLibraryExample
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
            var apiInstance = new AdLibraryApi(httpClient, config, httpClientHandler);
            var platform = "meta";  // string? | Which archive to search. `meta` needs no accountId. Required unless accountId is given. (optional) 
            var accountId = "accountId_example";  // string? | Zernio SocialAccount id. Required for LinkedIn (linkedin / linkedinads: its token searches). Optional for Meta, where any facebook / instagram / metaads account only selects the platform. (optional) 
            var q = "q_example";  // string? | Keyword search. Meta does not translate it, so write it in the ads' language. Required unless pageIds (Meta) or advertiser (LinkedIn) is given. (optional) 
            var pageIds = "pageIds_example";  // string? | Meta only. Comma-separated Facebook Page ids (max 10) whose ads to list. (optional) 
            var advertiser = "advertiser_example";  // string? | LinkedIn only. Advertiser (Page) name to search. (optional) 
            var countries = "countries_example";  // string? | Comma-separated ISO 3166-1 alpha-2 codes the ads reached. Meta defaults to ALL (an explicit ALL is Meta-only); LinkedIn searches every market when omitted. (optional) 
            var adType = "ALL";  // string? | Meta only. (optional)  (default to ALL)
            var status = "ACTIVE";  // string? | Meta only. ACTIVE = eligible for delivery right now. (optional)  (default to ACTIVE)
            var platforms = "platforms_example";  // string? | Meta only. Comma-separated publisher platforms: FACEBOOK, INSTAGRAM, AUDIENCE_NETWORK, MESSENGER, WHATSAPP, OCULUS, THREADS, STREAMING_SERVICES. (optional) 
            var mediaType = "ALL";  // string? | Meta only. (optional) 
            var languages = "languages_example";  // string? | Meta only. Comma-separated ISO 639-1 codes of the ad text. (optional) 
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | Meta only. Earliest delivery date (YYYY-MM-DD). LinkedIn's archive does not filter by date, so it is a 400 there: filter on details.adStatistics.firstImpressionAt / latestImpressionAt instead (EU-delivered ads only). (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | Meta only. Latest delivery date (YYYY-MM-DD); a 400 on LinkedIn, see since. (optional) 
            var searchType = "KEYWORD_UNORDERED";  // string? | Meta only. Whether q matches words in any order or as an exact phrase (comma-separate phrases to match all of them). (optional)  (default to KEYWORD_UNORDERED)
            var fields = id,page_name,ad_delivery_start_time,ad_creative_bodies;  // string? | Meta only. Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. (optional) 
            var limit = 25;  // int? | Rows per page. LinkedIn accepts at most 25. (optional)  (default to 25)
            var after = "after_example";  // string? | paging.after of the previous page. (optional) 

            try
            {
                // Search the public Ad Library
                SearchAdLibrary200Response result = apiInstance.SearchAdLibrary(platform, accountId, q, pageIds, advertiser, countries, adType, status, platforms, mediaType, languages, since, until, searchType, fields, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdLibraryApi.SearchAdLibrary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchAdLibraryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search the public Ad Library
    ApiResponse<SearchAdLibrary200Response> response = apiInstance.SearchAdLibraryWithHttpInfo(platform, accountId, q, pageIds, advertiser, countries, adType, status, platforms, mediaType, languages, since, until, searchType, fields, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdLibraryApi.SearchAdLibraryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **platform** | **string?** | Which archive to search. &#x60;meta&#x60; needs no accountId. Required unless accountId is given. | [optional]  |
| **accountId** | **string?** | Zernio SocialAccount id. Required for LinkedIn (linkedin / linkedinads: its token searches). Optional for Meta, where any facebook / instagram / metaads account only selects the platform. | [optional]  |
| **q** | **string?** | Keyword search. Meta does not translate it, so write it in the ads&#39; language. Required unless pageIds (Meta) or advertiser (LinkedIn) is given. | [optional]  |
| **pageIds** | **string?** | Meta only. Comma-separated Facebook Page ids (max 10) whose ads to list. | [optional]  |
| **advertiser** | **string?** | LinkedIn only. Advertiser (Page) name to search. | [optional]  |
| **countries** | **string?** | Comma-separated ISO 3166-1 alpha-2 codes the ads reached. Meta defaults to ALL (an explicit ALL is Meta-only); LinkedIn searches every market when omitted. | [optional]  |
| **adType** | **string?** | Meta only. | [optional] [default to ALL] |
| **status** | **string?** | Meta only. ACTIVE &#x3D; eligible for delivery right now. | [optional] [default to ACTIVE] |
| **platforms** | **string?** | Meta only. Comma-separated publisher platforms: FACEBOOK, INSTAGRAM, AUDIENCE_NETWORK, MESSENGER, WHATSAPP, OCULUS, THREADS, STREAMING_SERVICES. | [optional]  |
| **mediaType** | **string?** | Meta only. | [optional]  |
| **languages** | **string?** | Meta only. Comma-separated ISO 639-1 codes of the ad text. | [optional]  |
| **since** | **DateOnly?** | Meta only. Earliest delivery date (YYYY-MM-DD). LinkedIn&#39;s archive does not filter by date, so it is a 400 there: filter on details.adStatistics.firstImpressionAt / latestImpressionAt instead (EU-delivered ads only). | [optional]  |
| **until** | **DateOnly?** | Meta only. Latest delivery date (YYYY-MM-DD); a 400 on LinkedIn, see since. | [optional]  |
| **searchType** | **string?** | Meta only. Whether q matches words in any order or as an exact phrase (comma-separate phrases to match all of them). | [optional] [default to KEYWORD_UNORDERED] |
| **fields** | **string?** | Meta only. Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. | [optional]  |
| **limit** | **int?** | Rows per page. LinkedIn accepts at most 25. | [optional] [default to 25] |
| **after** | **string?** | paging.after of the previous page. | [optional]  |

### Return type

[**SearchAdLibrary200Response**](SearchAdLibrary200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Archived ads (raw platform shape) |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (legacy plans need the Ads add-on; included on usage-based plans), or &#x60;payment_required&#x60;: the billing owner has no payment method on file and no legacy paid plan. Searches are free; the card keeps the shared archive quota for real accounts. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted. Behavior per platform:  - **Reddit:** rate-limits per connected Reddit user (1000 requests per 10-minute window), shared by every operation on that account. Retry after the window resets; repeated calls while exhausted do not succeed and keep the budget spent. - **Google Ads:** writes and reports run on one developer token shared by every Google Ads account on Zernio. It holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. - **Google Ads envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **YouTube Analytics:** reads (channel-insights, demographics, daily-views, video-retention) use the \&quot;Queries per day\&quot; quota of the Google Cloud project the account is connected through, shared with other Zernio customers, so a 429 is not your own volume. Resets at midnight Pacific Time. - **YouTube Analytics envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **Meta ads:** every Meta throttle (codes 4, 17, 32, 613 and business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when sent, else Meta&#39;s 60-second minimum (30 seconds for the one-write-per-30-seconds limit on one object). - **Pinterest ads:** limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when sent, otherwise 60 seconds. - **TikTok ads:** limits per app and per endpoint (per second, minute and day), answering overage with code 40100 or code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (e.g. one ad at a time per advertiser) instead of retrying at once.  **TikTok Smart+ review read** (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has its own stricter TikTok quota. After an overage, Zernio answers 429 for that advertiser and connection without calling TikTok for about 60 seconds, then 120, up to 240 while TikTok keeps refusing, each with up to 10% random jitter.  A successful call holds nothing back; the next overage pauses about 60 seconds again. &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;retryAfterSeconds&#x60; and &#x60;refreshState&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |
| **501** | Only supported on Meta and LinkedIn accounts |  -  |
| **503** | Meta&#39;s Ad Library is unavailable on Zernio&#39;s side (&#x60;PLATFORM_DISABLED&#x60;); LinkedIn searches are unaffected. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

