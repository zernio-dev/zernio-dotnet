# Zernio.Api.MetricsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAccountMetrics**](MetricsApi.md#getaccountmetrics) | **GET** /v1/metrics/accounts | Read follower and post totals per account, platform or scope over time |
| [**GetAdAccountMetrics**](MetricsApi.md#getadaccountmetrics) | **GET** /v1/metrics/ad-accounts | Read the uploaded results summed across ad accounts |
| [**GetAdMetrics**](MetricsApi.md#getadmetrics) | **GET** /v1/metrics/ads | Read ad metrics by id, or one ad day by day with breakdowns |
| [**GetCampaignMetrics**](MetricsApi.md#getcampaignmetrics) | **GET** /v1/metrics/campaigns | Read the uploaded results of each campaign over a window |
| [**GetInboxMetrics**](MetricsApi.md#getinboxmetrics) | **GET** /v1/metrics/inbox | Read message volume and response times |
| [**GetInsightMetrics**](MetricsApi.md#getinsightmetrics) | **GET** /v1/metrics/insights | Read live account or post insights from the platform |
| [**GetMetricsCatalog**](MetricsApi.md#getmetricscatalog) | **GET** /v1/metrics/catalog | List the metrics, groupings and limits of each metrics endpoint |
| [**GetPostMetrics**](MetricsApi.md#getpostmetrics) | **GET** /v1/metrics/posts | Read post metrics by id, day by day, as a list, or grouped |
| [**QueryGoogleAds**](MetricsApi.md#querygoogleads) | **POST** /v1/metrics/platform-queries/google-ads | Run a Google Ads Query Language search on one customer |
| [**QueryGoogleAnalytics**](MetricsApi.md#querygoogleanalytics) | **POST** /v1/metrics/platform-queries/google-analytics | Run a GA4 standard or realtime report on one property |
| [**QueryMetaAds**](MetricsApi.md#querymetaads) | **POST** /v1/metrics/platform-queries/meta-ads | Run a Meta Marketing API insights query on one ad account |
| [**QueryTikTokAds**](MetricsApi.md#querytiktokads) | **POST** /v1/metrics/platform-queries/tiktok-ads | Run a TikTok Marketing API report on one advertiser |

<a id="getaccountmetrics"></a>
# **GetAccountMetrics**
> AccountMetricsResponse GetAccountMetrics (string? accountId = null, string? profileId = null, string? metrics = null, string? groupBy = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? platform = null, string? granularity = null, string? attribution = null, int? limit = null, string? cursor = null)

Read follower and post totals per account, platform or scope over time

Reads followers, the account counters the platform reports (media count, video count...) and the totals of the posts each account published, per account, per platform or for the whole scope, for the whole window or by day, week or month.  - Scope: exactly one of `accountId` (up to 25) or `profileId` (one, with an optional `platform`). - `groupBy`: `account` (the default, one row per account and period), `platform` or `none`. - `granularity`: `total` (the default), `day`, `week` (rows start on Monday) or `month`. A row's `date` is the start of its period, never before `fromDate`. - `attribution`: `publish` (the default) counts each post on the day it was published; `received` counts each interaction on the day it arrived, for windows up to 92 days. - `granularity=week&groupBy=platform&metrics=postCount,engagementRate`: how many posts each platform got per week and their pooled engagement rate. The newer way to read `GET /v1/analytics/posting-frequency`.  Without `fromDate` and `toDate` it reads the last 90 days; the window is at most 366 days. Followers are one value per day, taken at 02:00 UTC. `GET /v1/metrics/catalog?entity=accounts` lists every metric with the platforms that report it.  Each team has an analytics compute budget of 24 seconds per 30-second window across these reads: a request that would pass it is refused with 429 `details.scope: team_budget` before it runs.

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
    public class GetAccountMetricsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string? | Comma-separated account ids, up to 25. (optional) 
            var profileId = "profileId_example";  // string? | One profile id. (optional) 
            var metrics = "metrics_example";  // string? | Comma-separated metric names from the catalog. Defaults to every metric. (optional) 
            var groupBy = "groupBy_example";  // string? | Comma-separated groupings from the catalog, at most 2. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | First day, inclusive (YYYY-MM-DD, UTC). (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Last day, inclusive (YYYY-MM-DD, UTC). (optional) 
            var platform = "tiktok";  // string? | Only with profileId. (optional) 
            var granularity = "total";  // string? |  (optional)  (default to total)
            var attribution = "publish";  // string? |  (optional)  (default to publish)
            var limit = 50;  // int? | Rows per page, 50 by default, 100 at most. (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | pagination.nextCursor of the previous page, sent with the same query. (optional) 

            try
            {
                // Read follower and post totals per account, platform or scope over time
                AccountMetricsResponse result = apiInstance.GetAccountMetrics(accountId, profileId, metrics, groupBy, fromDate, toDate, platform, granularity, attribution, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetAccountMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAccountMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read follower and post totals per account, platform or scope over time
    ApiResponse<AccountMetricsResponse> response = apiInstance.GetAccountMetricsWithHttpInfo(accountId, profileId, metrics, groupBy, fromDate, toDate, platform, granularity, attribution, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetAccountMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string?** | Comma-separated account ids, up to 25. | [optional]  |
| **profileId** | **string?** | One profile id. | [optional]  |
| **metrics** | **string?** | Comma-separated metric names from the catalog. Defaults to every metric. | [optional]  |
| **groupBy** | **string?** | Comma-separated groupings from the catalog, at most 2. | [optional]  |
| **fromDate** | **DateOnly?** | First day, inclusive (YYYY-MM-DD, UTC). | [optional]  |
| **toDate** | **DateOnly?** | Last day, inclusive (YYYY-MM-DD, UTC). | [optional]  |
| **platform** | **string?** | Only with profileId. | [optional]  |
| **granularity** | **string?** |  | [optional] [default to total] |
| **attribution** | **string?** |  | [optional] [default to publish] |
| **limit** | **int?** | Rows per page, 50 by default, 100 at most. | [optional] [default to 50] |
| **cursor** | **string?** | pagination.nextCursor of the previous page, sent with the same query. | [optional]  |

### Return type

[**AccountMetricsResponse**](AccountMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One row per account, platform or scope, and period. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Analytics access required. Legacy plans need the Analytics add-on; included by default on usage-based plans. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadaccountmetrics"></a>
# **GetAdAccountMetrics**
> AdAccountMetricsResponse GetAdAccountMetrics (DateOnly fromDate, DateOnly toDate, string? adAccountId = null)

Read the uploaded results summed across ad accounts

Sums each result metric you uploaded across ad accounts (every ad account the key can read, or the platform ids in `adAccountId`) over `fromDate` to `toDate` (both required, at most 400 days), with the same metrics as `GET /v1/metrics/campaigns`.

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
    public class GetAdAccountMetricsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | First day, inclusive.
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly | Last day, inclusive. The range is at most 400 days.
            var adAccountId = "adAccountId_example";  // string? | Comma-separated platform ad account ids. Defaults to every ad account the key sees. (optional) 

            try
            {
                // Read the uploaded results summed across ad accounts
                AdAccountMetricsResponse result = apiInstance.GetAdAccountMetrics(fromDate, toDate, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetAdAccountMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdAccountMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read the uploaded results summed across ad accounts
    ApiResponse<AdAccountMetricsResponse> response = apiInstance.GetAdAccountMetricsWithHttpInfo(fromDate, toDate, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetAdAccountMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** | First day, inclusive. |  |
| **toDate** | **DateOnly** | Last day, inclusive. The range is at most 400 days. |  |
| **adAccountId** | **string?** | Comma-separated platform ad account ids. Defaults to every ad account the key sees. | [optional]  |

### Return type

[**AdAccountMetricsResponse**](AdAccountMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The results summed over the window. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;ads_addon_required&#x60;: the account has no ads access (included on usage-based plans). &#x60;insufficient_permissions&#x60;: the API key can read no profile. Also returned for a restricted key without the &#x60;ads&#x60; resource group. |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadmetrics"></a>
# **GetAdMetrics**
> AdMetricsResponse GetAdMetrics (string adId, string? granularity = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? breakdowns = null, string? attributionWindows = null)

Read ad metrics by id, or one ad day by day with breakdowns

Reads the delivery and conversion metrics Zernio synced from the ad networks for up to 100 Zernio ad ids (`adId`, as `GET /v1/ads` returns them). Ids you cannot read come back in `meta.missingIds`.  - `granularity=day` with one ad: one point per day. - `breakdowns` with one ad: read live from the network (age, gender, country, placement...), with `attributionWindows` for Meta.  Without `fromDate` and `toDate` it reads the last 90 days; the window is at most 730 days. `meta.backfillPending` is true while older days are still being fetched. Money is in the ad account currency (`currency`). `GET /v1/metrics/catalog?entity=ads` lists every metric with the networks that report it.

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
    public class GetAdMetricsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Comma-separated Zernio ad ids, up to 100.
            var granularity = "total";  // string? | day reads one ad, one point per day. (optional)  (default to total)
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Without fromDate and toDate, the last 90 days. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Last day, inclusive (YYYY-MM-DD, UTC). (optional) 
            var breakdowns = "breakdowns_example";  // string? | Comma-separated breakdowns, read live from the platform. One ad only. (optional) 
            var attributionWindows = "attributionWindows_example";  // string? | Meta attribution windows for the breakdowns, comma-separated. (optional) 

            try
            {
                // Read ad metrics by id, or one ad day by day with breakdowns
                AdMetricsResponse result = apiInstance.GetAdMetrics(adId, granularity, fromDate, toDate, breakdowns, attributionWindows);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetAdMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read ad metrics by id, or one ad day by day with breakdowns
    ApiResponse<AdMetricsResponse> response = apiInstance.GetAdMetricsWithHttpInfo(adId, granularity, fromDate, toDate, breakdowns, attributionWindows);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetAdMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Comma-separated Zernio ad ids, up to 100. |  |
| **granularity** | **string?** | day reads one ad, one point per day. | [optional] [default to total] |
| **fromDate** | **DateOnly?** | Without fromDate and toDate, the last 90 days. | [optional]  |
| **toDate** | **DateOnly?** | Last day, inclusive (YYYY-MM-DD, UTC). | [optional]  |
| **breakdowns** | **string?** | Comma-separated breakdowns, read live from the platform. One ad only. | [optional]  |
| **attributionWindows** | **string?** | Meta attribution windows for the breakdowns, comma-separated. | [optional]  |

### Return type

[**AdMetricsResponse**](AdMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One row per ad. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;ads_addon_required&#x60;: the account has no ads access (included on usage-based plans). &#x60;insufficient_permissions&#x60;: the API key can read no profile. Also returned for a restricted key without the &#x60;ads&#x60; resource group. |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignmetrics"></a>
# **GetCampaignMetrics**
> CampaignMetricsResponse GetCampaignMetrics (DateOnly fromDate, DateOnly toDate, int? limit = null, string? cursor = null, string? campaignId = null)

Read the uploaded results of each campaign over a window

Sums, per campaign, each result metric you uploaded (one key per metric, as `GET /v1/ads/campaign-results/metrics` lists them), with `cac_percent`, `cost_per_sale`, `cost_per_qualified_lead`, `lead_to_sale` and `qualified_rate` next to them, over `fromDate` to `toDate` (both required, at most 400 days).  Filter with `campaignId` (platform campaign ids); pages with `cursor`.

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
    public class GetCampaignMetricsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | First day, inclusive.
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly | Last day, inclusive. The range is at most 400 days.
            var limit = 50;  // int? | Rows per page, 50 by default, 100 at most. (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | pagination.nextCursor of the previous page, sent with the same query. (optional) 
            var campaignId = "campaignId_example";  // string? | Comma-separated platform campaign ids. (optional) 

            try
            {
                // Read the uploaded results of each campaign over a window
                CampaignMetricsResponse result = apiInstance.GetCampaignMetrics(fromDate, toDate, limit, cursor, campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetCampaignMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read the uploaded results of each campaign over a window
    ApiResponse<CampaignMetricsResponse> response = apiInstance.GetCampaignMetricsWithHttpInfo(fromDate, toDate, limit, cursor, campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetCampaignMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** | First day, inclusive. |  |
| **toDate** | **DateOnly** | Last day, inclusive. The range is at most 400 days. |  |
| **limit** | **int?** | Rows per page, 50 by default, 100 at most. | [optional] [default to 50] |
| **cursor** | **string?** | pagination.nextCursor of the previous page, sent with the same query. | [optional]  |
| **campaignId** | **string?** | Comma-separated platform campaign ids. | [optional]  |

### Return type

[**CampaignMetricsResponse**](CampaignMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One row per campaign with results in the window. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;ads_addon_required&#x60;: the account has no ads access (included on usage-based plans). &#x60;insufficient_permissions&#x60;: the API key can read no profile. Also returned for a restricted key without the &#x60;ads&#x60; resource group. |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxmetrics"></a>
# **GetInboxMetrics**
> InboxMetricsResponse GetInboxMetrics (string? conversationId = null, string? accountId = null, string? profileId = null, string? metrics = null, string? groupBy = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? platform = null, string? source = null, string? granularity = null, string? sort = null, string? include = null, int? limit = null, string? cursor = null)

Read message volume and response times

Counts messages received, sent, read and failed, conversations and replies, and response times (median, p90, p99, mean, min, max) across the inbox, from the messages Zernio logged.  - Scope: `conversationId` (up to 25, one row per conversation), `accountId` (up to 25) or one `profileId`. Without a scope, every account the key can read. - `groupBy` (at most 2): `account`, `platform`, `source`, `hourOfWeek` (one row per UTC weekday and hour), `responseTimeBucket` (with `metrics=replied`) or `conversation` (paged with `cursor`, `include=total` counts up to 100,000). - `granularity`: `total` (the default), `day` or `week`. - `include=account` adds usernames to account rows; `include=conversation` adds the participant and last message to conversation rows.  Response time metrics are returned only when named in `metrics`. Without `fromDate` and `toDate` it reads the last 30 days; the window is at most 90 days. `GET /v1/metrics/catalog?entity=inbox` lists every metric, sort and groupBy.

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
    public class GetInboxMetricsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string? | Comma-separated conversation ids (Zernio or platform), up to 25: one row per conversation. (optional) 
            var accountId = "accountId_example";  // string? | Comma-separated account ids, up to 25. (optional) 
            var profileId = "profileId_example";  // string? | One profile id. (optional) 
            var metrics = "metrics_example";  // string? | Comma-separated metric names from the catalog. Defaults to the counts; response times only when named. (optional) 
            var groupBy = "groupBy_example";  // string? | Comma-separated groupings from the catalog, at most 2: account, conversation, platform, source, hourOfWeek, responseTimeBucket. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | First day, inclusive (YYYY-MM-DD, UTC). Defaults to 30 days before toDate. The window is at most 90 days. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Last day, inclusive (YYYY-MM-DD, UTC). Defaults to today. (optional) 
            var platform = "platform_example";  // string? | A messaging platform, such as instagram or whatsapp. (optional) 
            var source = "source_example";  // string? | Only messages sent from this source, such as api or broadcast. Not with response time metrics. (optional) 
            var granularity = "total";  // string? |  (optional)  (default to total)
            var sort = "sort_example";  // string? | A sort from the catalog, such as messages-desc. With granularity=total. (optional) 
            var include = "include_example";  // string? | Comma-separated includes from the catalog: account, conversation, total. (optional) 
            var limit = 56;  // int? | Rows returned with groupBy=account (10 by default, 100 at most) or groupBy=conversation (50 by default, 1,000 at most). (optional) 
            var cursor = "cursor_example";  // string? | With groupBy=conversation: pagination.nextCursor of the previous page. (optional) 

            try
            {
                // Read message volume and response times
                InboxMetricsResponse result = apiInstance.GetInboxMetrics(conversationId, accountId, profileId, metrics, groupBy, fromDate, toDate, platform, source, granularity, sort, include, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetInboxMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read message volume and response times
    ApiResponse<InboxMetricsResponse> response = apiInstance.GetInboxMetricsWithHttpInfo(conversationId, accountId, profileId, metrics, groupBy, fromDate, toDate, platform, source, granularity, sort, include, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetInboxMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string?** | Comma-separated conversation ids (Zernio or platform), up to 25: one row per conversation. | [optional]  |
| **accountId** | **string?** | Comma-separated account ids, up to 25. | [optional]  |
| **profileId** | **string?** | One profile id. | [optional]  |
| **metrics** | **string?** | Comma-separated metric names from the catalog. Defaults to the counts; response times only when named. | [optional]  |
| **groupBy** | **string?** | Comma-separated groupings from the catalog, at most 2: account, conversation, platform, source, hourOfWeek, responseTimeBucket. | [optional]  |
| **fromDate** | **DateOnly?** | First day, inclusive (YYYY-MM-DD, UTC). Defaults to 30 days before toDate. The window is at most 90 days. | [optional]  |
| **toDate** | **DateOnly?** | Last day, inclusive (YYYY-MM-DD, UTC). Defaults to today. | [optional]  |
| **platform** | **string?** | A messaging platform, such as instagram or whatsapp. | [optional]  |
| **source** | **string?** | Only messages sent from this source, such as api or broadcast. Not with response time metrics. | [optional]  |
| **granularity** | **string?** |  | [optional] [default to total] |
| **sort** | **string?** | A sort from the catalog, such as messages-desc. With granularity&#x3D;total. | [optional]  |
| **include** | **string?** | Comma-separated includes from the catalog: account, conversation, total. | [optional]  |
| **limit** | **int?** | Rows returned with groupBy&#x3D;account (10 by default, 100 at most) or groupBy&#x3D;conversation (50 by default, 1,000 at most). | [optional]  |
| **cursor** | **string?** | With groupBy&#x3D;conversation: pagination.nextCursor of the previous page. | [optional]  |

### Return type

[**InboxMetricsResponse**](InboxMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One row per period and group. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinsightmetrics"></a>
# **GetInsightMetrics**
> InsightMetricsResponse GetInsightMetrics (string accountId, string? metrics = null, string? platformPostId = null, string? granularity = null, string? groupBy = null, string? breakdown = null, string? timeframe = null, string? cursor = null, int? limit = null, string? include = null, DateOnly? fromDate = null, DateOnly? toDate = null)

Read live account or post insights from the platform

Reads insights the platform computes and Zernio does not store (page views, profile visits, watch time, audience demographics...), live from the platform, for one account or one of its posts (`platformPostId`).  Platforms: Facebook, Instagram, LinkedIn, TikTok, YouTube, Pinterest, Google Business and Google Search Console. Another platform answers 400 on `accountId`, a disconnected account 401 `account_disconnected`, and a platform error the platform's own code under `platformError`.  - `granularity`: `total` (the default) or `day`. - `groupBy=demographic` with one metric and `breakdown` (age, gender, country, city...): one row per audience segment. LinkedIn: organizations only. - `groupBy=hour`: Instagram followers online per day and hour of the last 30 days. - `groupBy=keyword`: Google Business search keywords, one row per keyword, paged with `cursor`.  Google Search Console answers clicks, impressions, ctr (0 to 1) and position (1 is the top), final days only:  - Without groupBy: the site totals. `granularity=day` adds the date. - `groupBy` combines any of `query`, `page`, `country` and `device` (`groupBy=query,country`): one row per combination, most clicks first, with each value in `dimensions`. - Pages with `limit` (up to 25,000, 1,000 by default) and `cursor`. - `include=retentionCurve` with a YouTube `platformPostId`: the audience retention curve.  Without `fromDate` and `toDate` it reads the last 30 days; the window is at most 541 days. `GET /v1/metrics/catalog?entity=insights&platform=...` lists each platform's metrics. Metrics the platform cannot answer for this account are listed in `meta.unavailableMetrics` instead of failing the request.  Each request calls the platform: read each account every few minutes at most. These reads share the `account-insights` cap and the 120 reads per hour of one account.

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
    public class GetInsightMetricsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | One account id.
            var metrics = "metrics_example";  // string? | Comma-separated metric names (up to 25). Defaults to the platform's default metrics. `GET /v1/metrics/catalog?entity=insights&platform=...` lists them. (optional) 
            var platformPostId = "platformPostId_example";  // string? | One post of the account, by its platform id: answers the post's live insights instead of the account's. (optional) 
            var granularity = "total";  // string? | Defaults to total; groupBy=hour answers per day. (optional) 
            var groupBy = "groupBy_example";  // string? | demographic: audience segments (age, gender, country...). hour: Instagram followers online per day and hour, last 30 days. keyword: Google Business search keywords per month. query, page, country, device: Google Search Console, combined with commas (groupBy=query,country). (optional) 
            var breakdown = "breakdown_example";  // string? | With groupBy=demographic: comma-separated segments. Defaults to the platform's default segments. (optional) 
            var timeframe = "this_week";  // string? | Instagram demographics only. Defaults to this_month. (optional) 
            var cursor = "cursor_example";  // string? | With groupBy=keyword or a Search Console account: pagination.nextCursor of the previous page, sent with the same query. (optional) 
            var limit = 56;  // int? | Search Console accounts only: rows per page. Defaults to 1,000. (optional) 
            var include = "include_example";  // string? | With platformPostId on YouTube: retentionCurve adds the audience retention curve. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | First day, inclusive (YYYY-MM-DD, UTC). Defaults to 30 days before toDate. The window is at most 541 days. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Last day, inclusive (YYYY-MM-DD, UTC). Defaults to today. (optional) 

            try
            {
                // Read live account or post insights from the platform
                InsightMetricsResponse result = apiInstance.GetInsightMetrics(accountId, metrics, platformPostId, granularity, groupBy, breakdown, timeframe, cursor, limit, include, fromDate, toDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetInsightMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInsightMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read live account or post insights from the platform
    ApiResponse<InsightMetricsResponse> response = apiInstance.GetInsightMetricsWithHttpInfo(accountId, metrics, platformPostId, granularity, groupBy, breakdown, timeframe, cursor, limit, include, fromDate, toDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetInsightMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | One account id. |  |
| **metrics** | **string?** | Comma-separated metric names (up to 25). Defaults to the platform&#39;s default metrics. &#x60;GET /v1/metrics/catalog?entity&#x3D;insights&amp;platform&#x3D;...&#x60; lists them. | [optional]  |
| **platformPostId** | **string?** | One post of the account, by its platform id: answers the post&#39;s live insights instead of the account&#39;s. | [optional]  |
| **granularity** | **string?** | Defaults to total; groupBy&#x3D;hour answers per day. | [optional]  |
| **groupBy** | **string?** | demographic: audience segments (age, gender, country...). hour: Instagram followers online per day and hour, last 30 days. keyword: Google Business search keywords per month. query, page, country, device: Google Search Console, combined with commas (groupBy&#x3D;query,country). | [optional]  |
| **breakdown** | **string?** | With groupBy&#x3D;demographic: comma-separated segments. Defaults to the platform&#39;s default segments. | [optional]  |
| **timeframe** | **string?** | Instagram demographics only. Defaults to this_month. | [optional]  |
| **cursor** | **string?** | With groupBy&#x3D;keyword or a Search Console account: pagination.nextCursor of the previous page, sent with the same query. | [optional]  |
| **limit** | **int?** | Search Console accounts only: rows per page. Defaults to 1,000. | [optional]  |
| **include** | **string?** | With platformPostId on YouTube: retentionCurve adds the audience retention curve. | [optional]  |
| **fromDate** | **DateOnly?** | First day, inclusive (YYYY-MM-DD, UTC). Defaults to 30 days before toDate. The window is at most 541 days. | [optional]  |
| **toDate** | **DateOnly?** | Last day, inclusive (YYYY-MM-DD, UTC). Defaults to today. | [optional]  |

### Return type

[**InsightMetricsResponse**](InsightMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One row per period, or per segment with groupBy. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key, or the account is disconnected (&#x60;code: account_disconnected&#x60;, &#x60;action: reconnect&#x60;). |  -  |
| **402** | Analytics access required. Legacy plans need the Analytics add-on; included by default on usage-based plans. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getmetricscatalog"></a>
# **GetMetricsCatalog**
> MetricsCatalogResponse GetMetricsCatalog (string? entity = null, string? platform = null)

List the metrics, groupings and limits of each metrics endpoint

Describes each metrics endpoint (`GET /v1/metrics/posts`, `/accounts`, `/insights`, `/inbox`, `/ads`, `/campaigns` and `/ad-accounts`): the scope it needs, the most ids per scope, the longest and default date window, the granularities, sorts, includes, groupBy values, attributions and every metric with its unit, platforms and freshness.  Read it once and cache it: it changes only when Zernio adds a metric or a grouping. Filter with `entity` and `platform` to get only what one screen needs. No analytics add-on is needed to read it.

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
    public class GetMetricsCatalogExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var entity = "posts";  // string? | Only this entity. (optional) 
            var platform = "tiktok";  // string? | Only the metrics, sorts, includes and groupBy values this platform has. Every entity is still listed. (optional) 

            try
            {
                // List the metrics, groupings and limits of each metrics endpoint
                MetricsCatalogResponse result = apiInstance.GetMetricsCatalog(entity, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetMetricsCatalog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMetricsCatalogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List the metrics, groupings and limits of each metrics endpoint
    ApiResponse<MetricsCatalogResponse> response = apiInstance.GetMetricsCatalogWithHttpInfo(entity, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetMetricsCatalogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **entity** | **string?** | Only this entity. | [optional]  |
| **platform** | **string?** | Only the metrics, sorts, includes and groupBy values this platform has. Every entity is still listed. | [optional]  |

### Return type

[**MetricsCatalogResponse**](MetricsCatalogResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One entry per entity. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;campaign-analytics&#x60;, &#x60;ad-analytics&#x60;, &#x60;ads-listings&#x60;, &#x60;post-analytics&#x60; or &#x60;account-insights&#x60;: the team&#39;s analytics read cap for that group, on a 30-second sliding window. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level analytics endpoint.  |  * Retry-After - Seconds until card payments are tried again. <br>  * X-RateLimit-Limit - The ceiling of the limit that was reached. <br>  * X-RateLimit-Remaining - Requests remaining in the window. <br>  * X-RateLimit-Reset - Unix timestamp (seconds since epoch) when the next slot frees up. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getpostmetrics"></a>
# **GetPostMetrics**
> PostMetricsResponse GetPostMetrics (string? postId = null, string? platformPostId = null, string? accountId = null, string? profileId = null, string? metrics = null, string? groupBy = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? platform = null, string? granularity = null, string? origin = null, string? sort = null, string? include = null, string? changedSince = null, int? limit = null, string? cursor = null)

Read post metrics by id, day by day, as a list, or grouped

Reads the metrics Zernio synced for published posts, Zernio posts and posts published outside Zernio alike. Send exactly one scope: `postId`, `platformPostId`, `accountId` or `profileId`, or read the change feed with `changedSince`.  - **By id** (`postId` or `platformPostId`, up to 100): one row per publication. Ids that match no post you can read come back in `meta.missingIds`. - **One post day by day**: one id with `granularity=day`. - **A list** (`accountId` up to 25, or one `profileId` with an optional `platform`): posts published in the window, newest first, paged with `cursor`. `sort` orders it by a metric (`likes-desc`, `engagement-desc`...), up to the 1,000 best posts. `include=total` counts the list on the first page (windows up to 92 days).  Grouped with `groupBy`:  - `post`: sums the platforms each post id was published to into one row (by id, `granularity=total`). - `dayOfWeek,hour`: one row per UTC weekday and hour the posts were published, summing each post's latest metrics. The newer way to read `GET /v1/analytics/best-time`. - `postAge`: the share of its final engagement a post had reached at each age (0-6h to 30d+), `engagementShareOfFinal`. The newer way to read `GET /v1/analytics/content-decay`. Defaults to the last 60 days. - `format`: one row per format (image, video, carousel, text). The newer way to read `GET /v1/analytics/format-breakdown`.  `dayOfWeek,hour`, `postAge` and `format` take a list scope (`accountId` or `profileId`), `granularity=total`, windows up to 92 days, and answer in one page.  Includes on rows read by id or in a list (`include`, comma-separated):  - `post`: content, media and publishing details. - `samples`: one reading per analytics sync, oldest first, the newest 500 per post, narrowed by `fromDate` and `toDate` on the sync time. Posts read by `postId` or `platformPostId` only, up to 10, with `granularity=total` and no `groupBy`. The newer way to read `GET /v1/analytics/samples`. - `authenticity`: the stored authenticity score with its confidence, reasons, model version, sample count and when it was computed; null until the post has been scored. The `authenticityScore` metric carries the score alone (0 to 100). - `impressionSources`, `audienceTypes`, `audienceCountries`, `retentionCurve`: breakdowns on the platforms that report them.  Change feed with `changedSince`:  - `changedSince=now` answers no rows and a starting cursor; send each `pagination.nextCursor` back as `changedSince` to get one `PostMetricChange` row per post whose metrics changed since then, oldest change first. - It reads every account the key can read, narrowed with one `profileId` and `platform`. It takes `metrics` from the feed's list and the breakdown includes, nothing else. - Changes are kept 7 days and a cursor older than 6 days is refused. The feed and its cursors are the same as `GET /v1/analytics/delta`, of which it is the newer way to read.  Without `fromDate` and `toDate` a list reads the last 90 days; the window is at most 366 days. `GET /v1/metrics/catalog?entity=posts` lists every metric, sort, include and groupBy, with the platforms that report each. A metric is `null` when the platform does not report it or the post has no snapshot yet.  Each team has an analytics compute budget of 24 seconds per 30-second window across these reads, on top of the per-group cap: a request that would pass it is refused with 429 `details.scope: team_budget` before it runs.

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
    public class GetPostMetricsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var postId = "postId_example";  // string? | Comma-separated post ids (Zernio or external), up to 100. (optional) 
            var platformPostId = "platformPostId_example";  // string? | Comma-separated ids the platform gave the posts (a TikTok video id, a tweet id), up to 100. (optional) 
            var accountId = "accountId_example";  // string? | Comma-separated account ids, up to 25. (optional) 
            var profileId = "profileId_example";  // string? | One profile id. (optional) 
            var metrics = "metrics_example";  // string? | Comma-separated metric names from the catalog. Defaults to every metric. (optional) 
            var groupBy = "groupBy_example";  // string? | Comma-separated groupings from the catalog, at most 2. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | First day, inclusive (YYYY-MM-DD, UTC). (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Last day, inclusive (YYYY-MM-DD, UTC). (optional) 
            var platform = "tiktok";  // string? | Only with profileId. (optional) 
            var granularity = "total";  // string? | day reads one post. (optional)  (default to total)
            var origin = "all";  // string? | Lists only. Defaults to all. (optional) 
            var sort = "sort_example";  // string? | A sort from the catalog, such as published-desc or likes-desc. (optional) 
            var include = "include_example";  // string? | Comma-separated includes from the catalog. (optional) 
            var changedSince = "changedSince_example";  // string? | now (no rows, the starting cursor) or the previous pagination.nextCursor: one row per post whose metrics changed since, oldest first, across every account the key reads. Narrow with profileId and platform. Changes are kept 7 days; cursors older than 6 days are refused. (optional) 
            var limit = 50;  // int? | Rows per page, 50 by default, 100 at most. (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | pagination.nextCursor of the previous page, sent with the same query. (optional) 

            try
            {
                // Read post metrics by id, day by day, as a list, or grouped
                PostMetricsResponse result = apiInstance.GetPostMetrics(postId, platformPostId, accountId, profileId, metrics, groupBy, fromDate, toDate, platform, granularity, origin, sort, include, changedSince, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.GetPostMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPostMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read post metrics by id, day by day, as a list, or grouped
    ApiResponse<PostMetricsResponse> response = apiInstance.GetPostMetricsWithHttpInfo(postId, platformPostId, accountId, profileId, metrics, groupBy, fromDate, toDate, platform, granularity, origin, sort, include, changedSince, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.GetPostMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **postId** | **string?** | Comma-separated post ids (Zernio or external), up to 100. | [optional]  |
| **platformPostId** | **string?** | Comma-separated ids the platform gave the posts (a TikTok video id, a tweet id), up to 100. | [optional]  |
| **accountId** | **string?** | Comma-separated account ids, up to 25. | [optional]  |
| **profileId** | **string?** | One profile id. | [optional]  |
| **metrics** | **string?** | Comma-separated metric names from the catalog. Defaults to every metric. | [optional]  |
| **groupBy** | **string?** | Comma-separated groupings from the catalog, at most 2. | [optional]  |
| **fromDate** | **DateOnly?** | First day, inclusive (YYYY-MM-DD, UTC). | [optional]  |
| **toDate** | **DateOnly?** | Last day, inclusive (YYYY-MM-DD, UTC). | [optional]  |
| **platform** | **string?** | Only with profileId. | [optional]  |
| **granularity** | **string?** | day reads one post. | [optional] [default to total] |
| **origin** | **string?** | Lists only. Defaults to all. | [optional]  |
| **sort** | **string?** | A sort from the catalog, such as published-desc or likes-desc. | [optional]  |
| **include** | **string?** | Comma-separated includes from the catalog. | [optional]  |
| **changedSince** | **string?** | now (no rows, the starting cursor) or the previous pagination.nextCursor: one row per post whose metrics changed since, oldest first, across every account the key reads. Narrow with profileId and platform. Changes are kept 7 days; cursors older than 6 days are refused. | [optional]  |
| **limit** | **int?** | Rows per page, 50 by default, 100 at most. | [optional] [default to 50] |
| **cursor** | **string?** | pagination.nextCursor of the previous page, sent with the same query. | [optional]  |

### Return type

[**PostMetricsResponse**](PostMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rows of the shape the query asks for: &#x60;PostMetricRow&#x60; by id and in lists, &#x60;PostMetricGroup&#x60; with groupBy&#x3D;post, &#x60;PostMetricSlot&#x60; with groupBy&#x3D;dayOfWeek,hour, &#x60;PostMetricAge&#x60; with groupBy&#x3D;postAge, &#x60;PostMetricFormat&#x60; with groupBy&#x3D;format, &#x60;PostMetricChange&#x60; with changedSince. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Analytics access required. Legacy plans need the Analytics add-on; included by default on usage-based plans. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="querygoogleads"></a>
# **QueryGoogleAds**
> PlatformQueryPage QueryGoogleAds (GoogleAdsPlatformQueryBody googleAdsPlatformQueryBody)

Run a Google Ads Query Language search on one customer

Runs a GAQL `SELECT` on one Google Ads customer, read only. Without `adAccountId` it reads the connection's own customer.  Runs a native query on the platform with the account's own token and answers the platform's rows unchanged, with its own field names, plus its headers, counts and quota in `meta`. Use it for what `/v1/metrics/_*` does not store; the stored metrics stay cheaper and faster.  - Up to 120 reads per hour per platform target (the Zernio account plus the ad account or property); past it, 429 with `details.scope` `platform_query_target`.  - Up to 10 queries in flight per team.  - A query must answer within 25 seconds.  - An account of another source answers 400 on `accountId` with the route it belongs to.  - The next page goes in `cursor`, from `pagination.nextCursor`.

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
    public class QueryGoogleAdsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var googleAdsPlatformQueryBody = new GoogleAdsPlatformQueryBody(); // GoogleAdsPlatformQueryBody | 

            try
            {
                // Run a Google Ads Query Language search on one customer
                PlatformQueryPage result = apiInstance.QueryGoogleAds(googleAdsPlatformQueryBody);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.QueryGoogleAds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the QueryGoogleAdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run a Google Ads Query Language search on one customer
    ApiResponse<PlatformQueryPage> response = apiInstance.QueryGoogleAdsWithHttpInfo(googleAdsPlatformQueryBody);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.QueryGoogleAdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **googleAdsPlatformQueryBody** | [**GoogleAdsPlatformQueryBody**](GoogleAdsPlatformQueryBody.md) |  |  |

### Return type

[**PlatformQueryPage**](PlatformQueryPage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The platform&#39;s rows for the query. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;ads_addon_required&#x60;: the account has no ads access (included on usage-based plans). &#x60;insufficient_permissions&#x60;: the API key can read no profile. Also returned for a restricted key without the &#x60;ads&#x60; resource group. |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="querygoogleanalytics"></a>
# **QueryGoogleAnalytics**
> PlatformQueryPage QueryGoogleAnalytics (GoogleAnalyticsPlatformQueryBody googleAnalyticsPlatformQueryBody)

Run a GA4 standard or realtime report on one property

Runs a GA4 `standard` report over up to 4 date ranges, paged, or a `realtime` report on the last 30 minutes. Needs the Analytics add-on.  Runs a native query on the platform with the account's own token and answers the platform's rows unchanged, with its own field names, plus its headers, counts and quota in `meta`. Use it for what `/v1/metrics/_*` does not store; the stored metrics stay cheaper and faster.  - Up to 120 reads per hour per platform target (the Zernio account plus the ad account or property); past it, 429 with `details.scope` `platform_query_target`.  - Up to 10 queries in flight per team.  - A query must answer within 25 seconds.  - An account of another source answers 400 on `accountId` with the route it belongs to.  - The next page goes in `cursor`, from `pagination.nextCursor`.

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
    public class QueryGoogleAnalyticsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var googleAnalyticsPlatformQueryBody = new GoogleAnalyticsPlatformQueryBody(); // GoogleAnalyticsPlatformQueryBody | 

            try
            {
                // Run a GA4 standard or realtime report on one property
                PlatformQueryPage result = apiInstance.QueryGoogleAnalytics(googleAnalyticsPlatformQueryBody);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.QueryGoogleAnalytics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the QueryGoogleAnalyticsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run a GA4 standard or realtime report on one property
    ApiResponse<PlatformQueryPage> response = apiInstance.QueryGoogleAnalyticsWithHttpInfo(googleAnalyticsPlatformQueryBody);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.QueryGoogleAnalyticsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **googleAnalyticsPlatformQueryBody** | [**GoogleAnalyticsPlatformQueryBody**](GoogleAnalyticsPlatformQueryBody.md) |  |  |

### Return type

[**PlatformQueryPage**](PlatformQueryPage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The platform&#39;s rows for the query. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **402** | Analytics access required. Legacy plans need the Analytics add-on; included by default on usage-based plans. |  -  |
| **403** | The API key is a restricted key (zrk_ prefix) and may not perform this operation. Three cases:  1. The operation&#39;s resource group (see the operation&#39;s x-resource-group) is disabled on the key. Fix: create a key with the group enabled in the dashboard API keys tab and revoke the old one. 2. The operation is admin-plane (x-resource-group admin-plane: API keys, invites, connected apps, member identity), never grantable to restricted keys. The error reads \&quot;Restricted API keys cannot manage API keys, invites, or member identity.\&quot; Fix: a full-access key or the dashboard, never a new restricted key. 3. On webhook subscription writes, delivery-log reads and replays, a named event maps to a resource group the key does not hold. A restricted key can never create or edit a subscription broader than itself (a no-messages key cannot subscribe to, test-fire, redeliver or read logs for message.* events).  |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="querymetaads"></a>
# **QueryMetaAds**
> PlatformQueryPage QueryMetaAds (MetaAdsPlatformQueryBody metaAdsPlatformQueryBody)

Run a Meta Marketing API insights query on one ad account

Reads Meta's insights for one ad account (`act_<n>`). Read its campaigns, ad sets or ads with `level` and `filtering` on the same ad account.  Runs a native query on the platform with the account's own token and answers the platform's rows unchanged, with its own field names, plus its headers, counts and quota in `meta`. Use it for what `/v1/metrics/_*` does not store; the stored metrics stay cheaper and faster.  - Up to 120 reads per hour per platform target (the Zernio account plus the ad account or property); past it, 429 with `details.scope` `platform_query_target`.  - Up to 10 queries in flight per team.  - A query must answer within 25 seconds.  - An account of another source answers 400 on `accountId` with the route it belongs to.  - The next page goes in `cursor`, from `pagination.nextCursor`.

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
    public class QueryMetaAdsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var metaAdsPlatformQueryBody = new MetaAdsPlatformQueryBody(); // MetaAdsPlatformQueryBody | 

            try
            {
                // Run a Meta Marketing API insights query on one ad account
                PlatformQueryPage result = apiInstance.QueryMetaAds(metaAdsPlatformQueryBody);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.QueryMetaAds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the QueryMetaAdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run a Meta Marketing API insights query on one ad account
    ApiResponse<PlatformQueryPage> response = apiInstance.QueryMetaAdsWithHttpInfo(metaAdsPlatformQueryBody);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.QueryMetaAdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **metaAdsPlatformQueryBody** | [**MetaAdsPlatformQueryBody**](MetaAdsPlatformQueryBody.md) |  |  |

### Return type

[**PlatformQueryPage**](PlatformQueryPage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The platform&#39;s rows for the query. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;ads_addon_required&#x60;: the account has no ads access (included on usage-based plans). &#x60;insufficient_permissions&#x60;: the API key can read no profile. Also returned for a restricted key without the &#x60;ads&#x60; resource group. |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="querytiktokads"></a>
# **QueryTikTokAds**
> PlatformQueryPage QueryTikTokAds (TikTokAdsPlatformQueryBody tikTokAdsPlatformQueryBody)

Run a TikTok Marketing API report on one advertiser

Runs a synchronous TikTok report (`BASIC` or `AUDIENCE`) for one advertiser at the data level asked.  Runs a native query on the platform with the account's own token and answers the platform's rows unchanged, with its own field names, plus its headers, counts and quota in `meta`. Use it for what `/v1/metrics/_*` does not store; the stored metrics stay cheaper and faster.  - Up to 120 reads per hour per platform target (the Zernio account plus the ad account or property); past it, 429 with `details.scope` `platform_query_target`.  - Up to 10 queries in flight per team.  - A query must answer within 25 seconds.  - An account of another source answers 400 on `accountId` with the route it belongs to.  - The next page goes in `cursor`, from `pagination.nextCursor`.

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
    public class QueryTikTokAdsExample
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
            var apiInstance = new MetricsApi(httpClient, config, httpClientHandler);
            var tikTokAdsPlatformQueryBody = new TikTokAdsPlatformQueryBody(); // TikTokAdsPlatformQueryBody | 

            try
            {
                // Run a TikTok Marketing API report on one advertiser
                PlatformQueryPage result = apiInstance.QueryTikTokAds(tikTokAdsPlatformQueryBody);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetricsApi.QueryTikTokAds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the QueryTikTokAdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run a TikTok Marketing API report on one advertiser
    ApiResponse<PlatformQueryPage> response = apiInstance.QueryTikTokAdsWithHttpInfo(tikTokAdsPlatformQueryBody);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetricsApi.QueryTikTokAdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tikTokAdsPlatformQueryBody** | [**TikTokAdsPlatformQueryBody**](TikTokAdsPlatformQueryBody.md) |  |  |

### Return type

[**PlatformQueryPage**](PlatformQueryPage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The platform&#39;s rows for the query. |  -  |
| **400** | The query is invalid: an unknown or repeated parameter, a missing or second scope, a metric, groupBy, include or sort the entity does not have, or a window past its limit. &#x60;param&#x60; names the field. &#x60;GET /v1/metrics/catalog&#x60; lists what each entity accepts. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;ads_addon_required&#x60;: the account has no ads access (included on usage-based plans). &#x60;insufficient_permissions&#x60;: the API key can read no profile. Also returned for a restricted key without the &#x60;ads&#x60; resource group. |  -  |
| **429** | A limit on your request rate was reached. &#x60;details.scope&#x60; says which one:  - absent: your plan&#39;s API limit. - &#x60;post-analytics&#x60;, &#x60;account-insights&#x60;, &#x60;ad-analytics&#x60; or &#x60;campaign-analytics&#x60;: the team&#39;s cap of 300 reads per 30 seconds for that group. - &#x60;account_route&#x60;: 120 reads per hour of one account on one account-level endpoint. - &#x60;team_budget&#x60;: the team spent its analytics compute budget of 24 seconds per 30-second window. &#x60;Retry-After&#x60; counts to the end of the window. - &#x60;in_flight&#x60;: too many of the team&#39;s analytics reads are running at once.  &#x60;team_budget&#x60; and &#x60;in_flight&#x60; apply to posts, accounts, ads, campaigns and ad accounts reads. |  * Retry-After - Seconds until card payments are tried again. <br>  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

