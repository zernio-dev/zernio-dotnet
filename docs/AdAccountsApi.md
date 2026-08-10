# Zernio.Api.AdAccountsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCustomConversion**](AdAccountsApi.md#createcustomconversion) | **POST** /v1/accounts/{accountId}/custom-conversions | Create or reuse a custom conversion |
| [**CreateHighDemandPeriod**](AdAccountsApi.md#createhighdemandperiod) | **POST** /v1/ads/high-demand-periods | Schedule a budget increase |
| [**CreateValueRuleSet**](AdAccountsApi.md#createvalueruleset) | **POST** /v1/ads/value-rule-sets | Create a value rule set |
| [**DeleteValueRuleSet**](AdAccountsApi.md#deletevalueruleset) | **DELETE** /v1/ads/value-rule-sets/{valueRuleSetId} | Delete a value rule set |
| [**GetAdAccountFinance**](AdAccountsApi.md#getadaccountfinance) | **GET** /v1/ads/accounts/finance | Ad account finances |
| [**GetAdComments**](AdAccountsApi.md#getadcomments) | **GET** /v1/ads/{adId}/comments | List comments on an ad |
| [**GetAdsActivityLog**](AdAccountsApi.md#getadsactivitylog) | **GET** /v1/ads/activity | Ad account change / audit log |
| [**GetDsaDefaults**](AdAccountsApi.md#getdsadefaults) | **GET** /v1/ads/dsa-defaults | Get ad account DSA defaults |
| [**GetDsaRecommendations**](AdAccountsApi.md#getdsarecommendations) | **GET** /v1/ads/dsa-recommendations | List DSA beneficiary/payor suggestions |
| [**GetValueRuleSet**](AdAccountsApi.md#getvalueruleset) | **GET** /v1/ads/value-rule-sets/{valueRuleSetId} | Read a value rule set |
| [**ListAdAccounts**](AdAccountsApi.md#listadaccounts) | **GET** /v1/ads/accounts | List ad accounts |
| [**ListAdLabels**](AdAccountsApi.md#listadlabels) | **GET** /v1/ads/labels | Ad labels |
| [**ListAdStudies**](AdAccountsApi.md#listadstudies) | **GET** /v1/ads/studies | A/B tests and lift studies |
| [**ListAdsBusinessCenters**](AdAccountsApi.md#listadsbusinesscenters) | **GET** /v1/ads/business-centers | List TikTok Business Centers |
| [**ListCustomConversions**](AdAccountsApi.md#listcustomconversions) | **GET** /v1/accounts/{accountId}/custom-conversions | List custom conversions |
| [**ListHighDemandPeriods**](AdAccountsApi.md#listhighdemandperiods) | **GET** /v1/ads/high-demand-periods | High demand periods / budget schedules |
| [**ListMetaBusinesses**](AdAccountsApi.md#listmetabusinesses) | **GET** /v1/ads/businesses | Businesses list |
| [**ListValueRuleSets**](AdAccountsApi.md#listvaluerulesets) | **GET** /v1/ads/value-rule-sets | List value rule sets |
| [**UpdateAdAccount**](AdAccountsApi.md#updateadaccount) | **PATCH** /v1/ads/accounts | Update ad account settings |
| [**UpdateValueRuleSet**](AdAccountsApi.md#updatevalueruleset) | **PUT** /v1/ads/value-rule-sets/{valueRuleSetId} | Replace a value rule set |

<a id="createcustomconversion"></a>
# **CreateCustomConversion**
> CustomConversionResult CreateCustomConversion (string accountId, CreateCustomConversionRequest createCustomConversionRequest)

Create or reuse a custom conversion

Provision the Meta custom conversion an ads flow optimises toward, and hand back the `customConversionId` for `promotedObject.customConversionId` on POST /v1/ads/create. Removes the manual \"create it in Ads Manager first\" step.  **Reuse is ours, not Meta's.** Meta's create is not idempotent, so a retried request would otherwise mint a duplicate carrying none of the original's optimisation history. A non-archived conversion with the same `name` on the same `pixelId` is returned instead of created, with `reused: true` and a 200 rather than a 201.  `rule` is forwarded verbatim in Meta's own grammar (e.g. `{\"url\": {\"i_contains\": \"thank-you\"}}`); Meta validates it and rejects a malformed one with \"A conversion rule is required at creation time\".

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
    public class CreateCustomConversionExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Meta ads SocialAccount id.
            var createCustomConversionRequest = new CreateCustomConversionRequest(); // CreateCustomConversionRequest | 

            try
            {
                // Create or reuse a custom conversion
                CustomConversionResult result = apiInstance.CreateCustomConversion(accountId, createCustomConversionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateCustomConversion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCustomConversionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create or reuse a custom conversion
    ApiResponse<CustomConversionResult> response = apiInstance.CreateCustomConversionWithHttpInfo(accountId, createCustomConversionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateCustomConversionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Meta ads SocialAccount id. |  |
| **createCustomConversionRequest** | [**CreateCustomConversionRequest**](CreateCustomConversionRequest.md) |  |  |

### Return type

[**CustomConversionResult**](CustomConversionResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | An existing custom conversion was reused |  -  |
| **201** | Custom conversion created |  -  |
| **400** | Invalid input, or Meta rejected the conversion (bad rule, per-account cap reached) |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the token lacks the ads permissions. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createhighdemandperiod"></a>
# **CreateHighDemandPeriod**
> CreateHighDemandPeriod201Response CreateHighDemandPeriod (CreateHighDemandPeriodRequest createHighDemandPeriodRequest)

Schedule a budget increase

Pre-schedule a temporary budget increase (Black Friday, a launch, a sale) instead of editing the budget by hand on the day. Same target rule as the GET: exactly one of `campaignId` / `adSetId`.  Two Meta constraints worth knowing before you call it. `timeStart` / `timeEnd` must fall on a 15-minute boundary, and a campaign cannot mix `ABSOLUTE` and `MULTIPLIER` across its schedules — the second type is rejected with \"Can't mix your budget scaling selection\". Window rules (must sit inside the campaign's run dates, minimum lead time, no overlap) are Meta's and its message is forwarded verbatim.

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
    public class CreateHighDemandPeriodExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var createHighDemandPeriodRequest = new CreateHighDemandPeriodRequest(); // CreateHighDemandPeriodRequest | 

            try
            {
                // Schedule a budget increase
                CreateHighDemandPeriod201Response result = apiInstance.CreateHighDemandPeriod(createHighDemandPeriodRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateHighDemandPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateHighDemandPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule a budget increase
    ApiResponse<CreateHighDemandPeriod201Response> response = apiInstance.CreateHighDemandPeriodWithHttpInfo(createHighDemandPeriodRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateHighDemandPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createHighDemandPeriodRequest** | [**CreateHighDemandPeriodRequest**](CreateHighDemandPeriodRequest.md) |  |  |

### Return type

[**CreateHighDemandPeriod201Response**](CreateHighDemandPeriod201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Budget schedule created |  -  |
| **400** | Invalid input, or Meta rejected the schedule |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createvalueruleset"></a>
# **CreateValueRuleSet**
> CreateValueRuleSet201Response CreateValueRuleSet (CreateValueRuleSetRequest createValueRuleSetRequest)

Create a value rule set

Creates a value rule set on the ad account (Meta's `POST /act_X/value_rule_set`). Attach the returned id to an ad set with `valueRuleSetId` on `POST /v1/ads/create` or `PUT /v1/ads/ad-sets/{adSetId}`.  **Rule order is semantic**: rules are evaluated in array order and only the first matching rule adjusts the bid for an overlapping audience.  `adjustValue` is an unsigned magnitude in percent; the direction lives in `adjustSign`. `INCREASE` accepts 1-1000, `DECREASE` accepts 1-90. There is no signed field and 0 is out of range.  `criteriaValueTypes` is positionally paired with `criteriaValues` (same length, same order). Every type is the literal `\"NONE\"` except on `LOCATION`, which uses `LOCATION_COUNTRY` / `LOCATION_REGION` / `LOCATION_CITY` / `LOCATION_COMSCORE_MARKET` and may mix them within one criterion. Location values are Targeting-Search keys: a two-letter country code for `LOCATION_COUNTRY`, a numeric key for the rest.  `LOCATION_DMA` was replaced by `LOCATION_COMSCORE_MARKET` on 2026-06-22 and rules using DMAs are no longer active, so this API rejects it.  `AUDIENCE_LABEL` values (e.g. `HIGH_VALUE`) are applied to a Custom Audience in Ads Manager. There is no API to provision them, so label strings are passed through unvalidated and a typo produces a rule that never fires.  Ads Manager turns a rule set read-only (this API stays editable) when a rule uses more than 2 criteria, a custom age range, or the placements `FB_MARKETPLACE`, `FB_SEARCH`, `FB_VIDEO` or `IG_EXPLORE`.  Limits: 6 rule sets per ad account, 10 rules per set, 4 criteria per rule. The per-account cap is enforced by Meta, not here.

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
    public class CreateValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var createValueRuleSetRequest = new CreateValueRuleSetRequest(); // CreateValueRuleSetRequest | 

            try
            {
                // Create a value rule set
                CreateValueRuleSet201Response result = apiInstance.CreateValueRuleSet(createValueRuleSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.CreateValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a value rule set
    ApiResponse<CreateValueRuleSet201Response> response = apiInstance.CreateValueRuleSetWithHttpInfo(createValueRuleSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.CreateValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createValueRuleSetRequest** | [**CreateValueRuleSetRequest**](CreateValueRuleSetRequest.md) |  |  |

### Return type

[**CreateValueRuleSet201Response**](CreateValueRuleSet201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Value rule set created |  -  |
| **400** | Invalid input, or Meta rejected the create (per-account rule-set cap, ineligible criteria, or an account that is not enabled for value rules) |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletevalueruleset"></a>
# **DeleteValueRuleSet**
> DeleteValueRuleSet200Response DeleteValueRuleSet (string valueRuleSetId, string accountId)

Delete a value rule set

Deletes the rule set (Meta's `POST /{value-rule-set-id}/delete_rule_set`, a custom action edge rather than an HTTP DELETE on its side). Ad sets pointing at it are not modified here; detach them first with `valueRulesApplied: false` on `PUT /v1/ads/ad-sets/{adSetId}`.

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
    public class DeleteValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var valueRuleSetId = "valueRuleSetId_example";  // string | Platform value rule set id.
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.

            try
            {
                // Delete a value rule set
                DeleteValueRuleSet200Response result = apiInstance.DeleteValueRuleSet(valueRuleSetId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.DeleteValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a value rule set
    ApiResponse<DeleteValueRuleSet200Response> response = apiInstance.DeleteValueRuleSetWithHttpInfo(valueRuleSetId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.DeleteValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **valueRuleSetId** | **string** | Platform value rule set id. |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |

### Return type

[**DeleteValueRuleSet200Response**](DeleteValueRuleSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Value rule set deleted |  -  |
| **400** | Invalid input, or Meta rejected the delete. A bad id comes back as GraphMethodException code 100 / subcode 33, which reads like a permission error rather than a 404. |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadaccountfinance"></a>
# **GetAdAccountFinance**
> GetAdAccountFinance200Response GetAdAccountFinance (string accountId, string adAccountId)

Ad account finances

Finances of one Meta ad account: prepaid `balance`, lifetime `amountSpent`, account `spendCap` (null = no cap) and the `fundingSource`. Money values are converted from Meta's minor units to whole units of `currency`.

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
    public class GetAdAccountFinanceExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).

            try
            {
                // Ad account finances
                GetAdAccountFinance200Response result = apiInstance.GetAdAccountFinance(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetAdAccountFinance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdAccountFinanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad account finances
    ApiResponse<GetAdAccountFinance200Response> response = apiInstance.GetAdAccountFinanceWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetAdAccountFinanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |

### Return type

[**GetAdAccountFinance200Response**](GetAdAccountFinance200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account finances |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcomments"></a>
# **GetAdComments**
> GetAdComments200Response GetAdComments (string adId, string? placement = null, int? limit = null, string? cursor = null)

List comments on an ad

Returns comments on an ad's underlying creative post. Useful for moderating or analyzing engagement on dark posts (ad creatives that never went live organically), which the regular GET /v1/inbox/comments/{postId} endpoint cannot serve because dark posts are not in Zernio's post database.  An ad that runs on both Facebook feed and Instagram feed has two separate underlying posts with separate comment threads (the creative's effective_object_story_id and effective_instagram_media_id). Use the `placement` query param to pick one; with no param the Instagram side is returned when it exists, otherwise Facebook. The identifiers are read from the ad record (persisted during sync) with a Marketing-API fallback for ads that predate the field.  For Instagram-placed comments, the Instagram account that runs the ad must be connected to Zernio — those comments are read through that account's token. If no connected Instagram account on the profile can read the ad's media, the call returns ads_connection_required (the Facebook side, if any, is still readable via ?placement=facebook).  Meta-only. Other ad platforms (TikTok, LinkedIn, Pinterest, Google, X) do not expose a public per-ad comments API and return feature_not_available.  Requires the Ads add-on. Response shape matches GET /v1/inbox/comments/{postId}.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: Zernio internal `_id` (24-char hex), Meta's numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`), or the creative's `effective_object_story_id` / `effective_instagram_media_id`. Caller doesn't need a translation step. 

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
    public class GetAdCommentsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Internal Zernio ad ID (ObjectId).
            var placement = "facebook";  // string? | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. (optional) 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? | Pagination cursor from a previous response. (optional) 

            try
            {
                // List comments on an ad
                GetAdComments200Response result = apiInstance.GetAdComments(adId, placement, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetAdComments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCommentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List comments on an ad
    ApiResponse<GetAdComments200Response> response = apiInstance.GetAdCommentsWithHttpInfo(adId, placement, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetAdCommentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Internal Zernio ad ID (ObjectId). |  |
| **placement** | **string?** | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** | Pagination cursor from a previous response. | [optional]  |

### Return type

[**GetAdComments200Response**](GetAdComments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comments on the ad |  -  |
| **400** | Invalid ad ID format, or the ad&#39;s creative format does not expose a commentable underlying post (code ad_not_commentable).  |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (legacy plans need the Ads add-on; included by default on usage-based plans), or ad platform is not Meta (code feature_not_available). |  -  |
| **404** | Resource not found |  -  |
| **422** | Ads account token unavailable, or (for Instagram-placed ads) no connected Instagram account on the profile can read the ad&#39;s media (code ads_connection_required).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadsactivitylog"></a>
# **GetAdsActivityLog**
> GetAdsActivityLog200Response GetAdsActivityLog (string accountId, string adAccountId, DateOnly? since = null, DateOnly? until = null, string? objectId = null, int? limit = null, string? after = null)

Ad account change / audit log

Account-level audit log from Meta's `/act_X/activities`: who changed what and when (creates, edits, status flips, budget changes...) with Meta's translated event names and the structured before/after in `extra_data`. Rows are returned verbatim. Meta has no server-side per-object filter on this edge, so `objectId` filters the returned page client-side (combine with paging to walk history for one campaign/ad set/ad).

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
    public class GetAdsActivityLogExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var since = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of range (YYYY-MM-DD). (optional) 
            var until = DateOnly.Parse("2013-10-20");  // DateOnly? | End of range (YYYY-MM-DD). (optional) 
            var objectId = "objectId_example";  // string? | Client-side filter to one Meta object id (campaign, ad set or ad). (optional) 
            var limit = 50;  // int? | Rows per page (optional)  (default to 50)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Ad account change / audit log
                GetAdsActivityLog200Response result = apiInstance.GetAdsActivityLog(accountId, adAccountId, since, until, objectId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetAdsActivityLog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdsActivityLogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad account change / audit log
    ApiResponse<GetAdsActivityLog200Response> response = apiInstance.GetAdsActivityLogWithHttpInfo(accountId, adAccountId, since, until, objectId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetAdsActivityLogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **since** | **DateOnly?** | Start of range (YYYY-MM-DD). | [optional]  |
| **until** | **DateOnly?** | End of range (YYYY-MM-DD). | [optional]  |
| **objectId** | **string?** | Client-side filter to one Meta object id (campaign, ad set or ad). | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 50] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**GetAdsActivityLog200Response**](GetAdsActivityLog200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Activity rows (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdsadefaults"></a>
# **GetDsaDefaults**
> UpdateAdAccount200Response GetDsaDefaults (string accountId, string adAccountId)

Get ad account DSA defaults

Returns the default DSA beneficiary and payor currently set on a Meta ad account, whether they were set via `PATCH /v1/ads/accounts` or in Meta Ads Manager. Fields are omitted when no default is configured. Meta accounts only. 

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
    public class GetDsaDefaultsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Social account ID (metaads, or a facebook/instagram posting account)
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID (act_...)

            try
            {
                // Get ad account DSA defaults
                UpdateAdAccount200Response result = apiInstance.GetDsaDefaults(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetDsaDefaults: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDsaDefaultsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ad account DSA defaults
    ApiResponse<UpdateAdAccount200Response> response = apiInstance.GetDsaDefaultsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetDsaDefaultsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Social account ID (metaads, or a facebook/instagram posting account) |  |
| **adAccountId** | **string** | Meta ad account ID (act_...) |  |

### Return type

[**UpdateAdAccount200Response**](UpdateAdAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Current DSA defaults (empty object when none are set) |  -  |
| **400** | Non-Meta adAccountId |  -  |
| **401** | Unauthorized |  -  |
| **404** | Social account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getdsarecommendations"></a>
# **GetDsaRecommendations**
> GetDsaRecommendations200Response GetDsaRecommendations (string accountId, string adAccountId)

List DSA beneficiary/payor suggestions

Returns Meta's suggested beneficiary/payor names for an ad account, derived by Meta from the account's recent activity. Useful for prefilling `dsaBeneficiary`/`dsaPayor` inputs, or the defaults sent to `PATCH /v1/ads/accounts`, in your own UI.  Meta returns a single flat list. Entries are not labeled as beneficiary or payor, and since these are legal disclosures Zernio never applies them automatically: let your user pick the right entity. The list may be empty for accounts with little activity. Meta accounts only. 

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
    public class GetDsaRecommendationsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Social account ID (metaads, or a facebook/instagram posting account)
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID (act_...)

            try
            {
                // List DSA beneficiary/payor suggestions
                GetDsaRecommendations200Response result = apiInstance.GetDsaRecommendations(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetDsaRecommendations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDsaRecommendationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List DSA beneficiary/payor suggestions
    ApiResponse<GetDsaRecommendations200Response> response = apiInstance.GetDsaRecommendationsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetDsaRecommendationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Social account ID (metaads, or a facebook/instagram posting account) |  |
| **adAccountId** | **string** | Meta ad account ID (act_...) |  |

### Return type

[**GetDsaRecommendations200Response**](GetDsaRecommendations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Suggested DSA strings (may be empty when Meta has no recommendations) |  -  |
| **400** | Non-Meta adAccountId |  -  |
| **401** | Unauthorized |  -  |
| **404** | Social account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getvalueruleset"></a>
# **GetValueRuleSet**
> GetValueRuleSet200Response GetValueRuleSet (string valueRuleSetId, string accountId)

Read a value rule set

Reads one value rule set including every nested rule id and criterion id. This is step one of any edit: `PUT` is a full replace, so you need the ids before you can keep the objects you are not changing.  Meta's own read returns `GENDER` values lowercase (`\"male\"`) while writes require `\"MALE\"`. Values are passed through untouched, so never case-compare a stored rule against a fetched one.

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
    public class GetValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var valueRuleSetId = "valueRuleSetId_example";  // string | Platform value rule set id.
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.

            try
            {
                // Read a value rule set
                GetValueRuleSet200Response result = apiInstance.GetValueRuleSet(valueRuleSetId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.GetValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a value rule set
    ApiResponse<GetValueRuleSet200Response> response = apiInstance.GetValueRuleSetWithHttpInfo(valueRuleSetId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.GetValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **valueRuleSetId** | **string** | Platform value rule set id. |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |

### Return type

[**GetValueRuleSet200Response**](GetValueRuleSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Value rule set |  -  |
| **400** | Invalid input, or Meta rejected the read. A bad id comes back as GraphMethodException code 100 / subcode 33, which cannot be told apart from a permission problem. |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadaccounts"></a>
# **ListAdAccounts**
> ListAdAccounts200Response ListAdAccounts (string accountId, string? adAccountId = null, int? limit = null)

List ad accounts

Returns the platform ad accounts available for the given social account (e.g. Meta ad accounts, TikTok advertiser IDs, Google Ads customer IDs).  For TikTok agencies: enumerates every advertiser under every Business Center the token can read (paginated server-side), then chunks the lookup against TikTok's `/advertiser/info/` endpoint (which has a per-call cap of ≤100 IDs). Solo advertisers without a BC fall back to the OAuth-time `advertiser_ids` list. Cached for 1h on the SocialAccount; lazy-refreshed on first call after expiry.  For Google Ads: responds `429` when Google's API quota is temporarily exhausted (instead of an empty list). Retry after a delay. 

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
    public class ListAdAccountsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Social account ID
            var adAccountId = "adAccountId_example";  // string? | Filter response to a single platform ad account ID (e.g. `act_123` for Meta, advertiser_id for TikTok). Returns at most one item. (optional) 
            var limit = 56;  // int? | Clamp the returned `accounts[]` length. Useful for typeahead pickers on agency tokens with hundreds of advertisers. (optional) 

            try
            {
                // List ad accounts
                ListAdAccounts200Response result = apiInstance.ListAdAccounts(accountId, adAccountId, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ad accounts
    ApiResponse<ListAdAccounts200Response> response = apiInstance.ListAdAccountsWithHttpInfo(accountId, adAccountId, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Social account ID |  |
| **adAccountId** | **string?** | Filter response to a single platform ad account ID (e.g. &#x60;act_123&#x60; for Meta, advertiser_id for TikTok). Returns at most one item. | [optional]  |
| **limit** | **int?** | Clamp the returned &#x60;accounts[]&#x60; length. Useful for typeahead pickers on agency tokens with hundreds of advertisers. | [optional]  |

### Return type

[**ListAdAccounts200Response**](ListAdAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad accounts |  -  |
| **401** | Unauthorized |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads) or Instagram missing linked Facebook account |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted.  Reddit rate-limits per connected Reddit user (1000 requests per 10-minute window), and that budget is shared by every operation using that account. Retry after the window resets rather than retrying immediately; repeated calls while exhausted do not succeed and keep the budget spent.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadlabels"></a>
# **ListAdLabels**
> ListAdLabels200Response ListAdLabels (string accountId, string adAccountId, int? limit = null, string? after = null)

Ad labels

Lists the ad account's organizational labels (Meta's `/act_X/adlabels`), rows returned verbatim (id, name, created/updated time).

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
    public class ListAdLabelsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Ad labels
                ListAdLabels200Response result = apiInstance.ListAdLabels(accountId, adAccountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad labels
    ApiResponse<ListAdLabels200Response> response = apiInstance.ListAdLabelsWithHttpInfo(accountId, adAccountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdLabelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListAdLabels200Response**](ListAdLabels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad labels (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadstudies"></a>
# **ListAdStudies**
> ListAdStudies200Response ListAdStudies (string accountId, string adAccountId, string? fields = null, int? limit = null, string? after = null)

A/B tests and lift studies

Lists the ad account's A/B tests and lift studies (Meta's `/act_X/ad_studies`), rows returned verbatim. The default projection covers id, name, type, timing and cells with split percentages; `fields` is a raw-passthrough override.

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
    public class ListAdStudiesExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var fields = "fields_example";  // string? | Comma-separated Graph field override (supports nested {} projections). (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // A/B tests and lift studies
                ListAdStudies200Response result = apiInstance.ListAdStudies(accountId, adAccountId, fields, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdStudies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdStudiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // A/B tests and lift studies
    ApiResponse<ListAdStudies200Response> response = apiInstance.ListAdStudiesWithHttpInfo(accountId, adAccountId, fields, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdStudiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **fields** | **string?** | Comma-separated Graph field override (supports nested {} projections). | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListAdStudies200Response**](ListAdStudies200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad studies (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadsbusinesscenters"></a>
# **ListAdsBusinessCenters**
> ListAdsBusinessCenters200Response ListAdsBusinessCenters (string accountId)

List TikTok Business Centers

Returns the TikTok Business Centers (BCs) the connected `tiktokads` account can read. Each BC reports its advertiser count so callers can build agency-style pickers without re-walking `/v1/ads/accounts` per BC.  TikTok-only. Solo advertisers (non-agency tokens) return an empty array. 

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
    public class ListAdsBusinessCentersExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | ID of the `tiktokads` (or parent `tiktok` posting) SocialAccount

            try
            {
                // List TikTok Business Centers
                ListAdsBusinessCenters200Response result = apiInstance.ListAdsBusinessCenters(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListAdsBusinessCenters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdsBusinessCentersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List TikTok Business Centers
    ApiResponse<ListAdsBusinessCenters200Response> response = apiInstance.ListAdsBusinessCentersWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListAdsBusinessCentersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | ID of the &#x60;tiktokads&#x60; (or parent &#x60;tiktok&#x60; posting) SocialAccount |  |

### Return type

[**ListAdsBusinessCenters200Response**](ListAdsBusinessCenters200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Business centers |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | TikTok account not found |  -  |
| **422** | TikTok Ads not connected |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcustomconversions"></a>
# **ListCustomConversions**
> ListCustomConversions200Response ListCustomConversions (string accountId, string adAccountId)

List custom conversions

The ad account's Meta custom conversions, including archived ones (`isArchived`).

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
    public class ListCustomConversionsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Meta ads SocialAccount id.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).

            try
            {
                // List custom conversions
                ListCustomConversions200Response result = apiInstance.ListCustomConversions(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListCustomConversions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCustomConversionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List custom conversions
    ApiResponse<ListCustomConversions200Response> response = apiInstance.ListCustomConversionsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListCustomConversionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Meta ads SocialAccount id. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |

### Return type

[**ListCustomConversions200Response**](ListCustomConversions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom conversions |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the token lacks the ads permissions. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listhighdemandperiods"></a>
# **ListHighDemandPeriods**
> ListHighDemandPeriods200Response ListHighDemandPeriods (string accountId, string? campaignId = null, string? adSetId = null, int? limit = null, string? after = null)

High demand periods / budget schedules

Scheduled budget increases (Meta's budget-scheduling API). The Graph edge lives on the campaign and ad-set nodes only, so exactly one of `campaignId` / `adSetId` (platform ids) is required. Rows returned verbatim (budget_value, budget_value_type, time window, recurrence).

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
    public class ListHighDemandPeriodsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var campaignId = "campaignId_example";  // string? | Platform campaign id. Exactly one of campaignId / adSetId. (optional) 
            var adSetId = "adSetId_example";  // string? | Platform ad set id. Exactly one of campaignId / adSetId. (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // High demand periods / budget schedules
                ListHighDemandPeriods200Response result = apiInstance.ListHighDemandPeriods(accountId, campaignId, adSetId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListHighDemandPeriods: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListHighDemandPeriodsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // High demand periods / budget schedules
    ApiResponse<ListHighDemandPeriods200Response> response = apiInstance.ListHighDemandPeriodsWithHttpInfo(accountId, campaignId, adSetId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListHighDemandPeriodsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **campaignId** | **string?** | Platform campaign id. Exactly one of campaignId / adSetId. | [optional]  |
| **adSetId** | **string?** | Platform ad set id. Exactly one of campaignId / adSetId. | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListHighDemandPeriods200Response**](ListHighDemandPeriods200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Budget schedules (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listmetabusinesses"></a>
# **ListMetaBusinesses**
> ListMetaBusinesses200Response ListMetaBusinesses (string accountId, int? limit = null, string? after = null)

Businesses list

Business Manager portfolios the connected Meta user belongs to (Meta's `/me/businesses`), rows returned verbatim (id, name, verification_status, created_time). Token-scoped, so no `adAccountId` is needed. For TikTok Business Centers use `GET /v1/ads/business-centers`.

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
    public class ListMetaBusinessesExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Businesses list
                ListMetaBusinesses200Response result = apiInstance.ListMetaBusinesses(accountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListMetaBusinesses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListMetaBusinessesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Businesses list
    ApiResponse<ListMetaBusinesses200Response> response = apiInstance.ListMetaBusinessesWithHttpInfo(accountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListMetaBusinessesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListMetaBusinesses200Response**](ListMetaBusinesses200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Businesses (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listvaluerulesets"></a>
# **ListValueRuleSets**
> ListValueRuleSets200Response ListValueRuleSets (string accountId, string adAccountId, int? limit = null, string? after = null)

List value rule sets

Lists the ad account's value rule sets (Meta's `/act_X/value_rule_set`). A value rule set adjusts the auction bid up or down for audience segments you value differently; attach one to an ad set with `valueRuleSetId` on `POST /v1/ads/create` or `PUT /v1/ads/ad-sets/{adSetId}`.  Rows are returned in the same camelCase shape the `PUT` body takes, ids included, so a set round-trips 1:1: **the update is a full replace, not a patch**, so you GET, mutate and send the whole thing back.  Limits: 6 rule sets per ad account, 10 rules per set, 4 criteria per rule.  **Rule order is semantic.** Rules are evaluated in array order and only the FIRST matching rule adjusts the bid for an overlapping audience. The order you send is the order that is stored and returned.  Eligibility: value rule sets apply only to ad sets on the `LOWEST_COST_WITHOUT_CAP` (auto-bid) or `COST_CAP` bid strategies. Meta rejects the rest server-side.

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
    public class ListValueRuleSetsExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. Meta does not document paging on this edge; `after` comes back null when it omits cursors. (optional) 

            try
            {
                // List value rule sets
                ListValueRuleSets200Response result = apiInstance.ListValueRuleSets(accountId, adAccountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.ListValueRuleSets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListValueRuleSetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List value rule sets
    ApiResponse<ListValueRuleSets200Response> response = apiInstance.ListValueRuleSetsWithHttpInfo(accountId, adAccountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.ListValueRuleSetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. Meta does not document paging on this edge; &#x60;after&#x60; comes back null when it omits cursors. | [optional]  |

### Return type

[**ListValueRuleSets200Response**](ListValueRuleSets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Value rule sets |  -  |
| **400** | Invalid input, or Meta rejected the query. Meta answers a bad rule-set id with GraphMethodException code 100 / subcode 33, which is indistinguishable between not-found, no-permission, and account-not-enabled. |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadaccount"></a>
# **UpdateAdAccount**
> UpdateAdAccount200Response UpdateAdAccount (UpdateAdAccountRequest updateAdAccountRequest)

Update ad account settings

Sets the default DSA beneficiary and payor on a Meta ad account (EU DSA, Article 26). Set them once and every EU-targeted call to `/v1/ads/create`, `/v1/ads/boost` and `/v1/ads/ctwa` on that ad account can omit `dsaBeneficiary`/`dsaPayor`: Meta applies the defaults automatically.  The values are written to the ad account on Meta, the same setting Ads Manager edits. Nothing is stored in Zernio, and defaults already set in Ads Manager work identically. Zernio never guesses these values for you. Beneficiary and payor are legal disclosures shown to EU users, so you must provide the entity names explicitly. Use `GET /v1/ads/dsa-recommendations` to offer suggestions in your UI.  If `defaultDsaPayor` is omitted, the beneficiary is also set as the payor, which covers the common case where the same entity benefits from and pays for the ads. Read the current values back with `GET /v1/ads/dsa-defaults`.  Currently supported for Meta accounts only; other platforms return 400. 

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
    public class UpdateAdAccountExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var updateAdAccountRequest = new UpdateAdAccountRequest(); // UpdateAdAccountRequest | 

            try
            {
                // Update ad account settings
                UpdateAdAccount200Response result = apiInstance.UpdateAdAccount(updateAdAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateAdAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update ad account settings
    ApiResponse<UpdateAdAccount200Response> response = apiInstance.UpdateAdAccountWithHttpInfo(updateAdAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateAdAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateAdAccountRequest** | [**UpdateAdAccountRequest**](UpdateAdAccountRequest.md) |  |  |

### Return type

[**UpdateAdAccount200Response**](UpdateAdAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DSA defaults updated (re-read from Meta after the write) |  -  |
| **400** | Unsupported platform (non-Meta account) or invalid adAccountId |  -  |
| **401** | Unauthorized |  -  |
| **404** | Social account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatevalueruleset"></a>
# **UpdateValueRuleSet**
> UpdateValueRuleSet200Response UpdateValueRuleSet (string valueRuleSetId, UpdateValueRuleSetRequest updateValueRuleSetRequest)

Replace a value rule set

**THIS IS A FULL REPLACE, NOT A PATCH.** Meta's update is declarative: the body you send becomes the rule set.  - `GET /v1/ads/value-rule-sets/{valueRuleSetId}` FIRST. - Keep a rule or criterion by echoing its `id`. - Create one by including the object WITHOUT an `id`. - Delete one by OMITTING it from the array. There is no warning and no undo.  `name` and `rules` are both required for exactly this reason: a partial body would silently destroy every rule left out.  **Rule order is semantic**: the array order you send is the evaluation order, and only the first matching rule adjusts the bid for an overlapping audience.  Existing rule sets created elsewhere may contain `LOCATION_DMA` criteria. Those went inert on 2026-06-22 and are rejected here; migrate them to `LOCATION_COMSCORE_MARKET`.

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
    public class UpdateValueRuleSetExample
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
            var apiInstance = new AdAccountsApi(httpClient, config, httpClientHandler);
            var valueRuleSetId = "valueRuleSetId_example";  // string | Platform value rule set id.
            var updateValueRuleSetRequest = new UpdateValueRuleSetRequest(); // UpdateValueRuleSetRequest | 

            try
            {
                // Replace a value rule set
                UpdateValueRuleSet200Response result = apiInstance.UpdateValueRuleSet(valueRuleSetId, updateValueRuleSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdAccountsApi.UpdateValueRuleSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateValueRuleSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace a value rule set
    ApiResponse<UpdateValueRuleSet200Response> response = apiInstance.UpdateValueRuleSetWithHttpInfo(valueRuleSetId, updateValueRuleSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdAccountsApi.UpdateValueRuleSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **valueRuleSetId** | **string** | Platform value rule set id. |  |
| **updateValueRuleSetRequest** | [**UpdateValueRuleSetRequest**](UpdateValueRuleSetRequest.md) |  |  |

### Return type

[**UpdateValueRuleSet200Response**](UpdateValueRuleSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Value rule set replaced |  -  |
| **400** | Invalid input, or Meta rejected the update |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

