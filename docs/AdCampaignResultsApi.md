# Zernio.Api.AdCampaignResultsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCampaignResultsUpload**](AdCampaignResultsApi.md#getcampaignresultsupload) | **GET** /v1/ads/campaign-results/uploads/{uploadId} | Check a results upload |
| [**ListCampaignResultMetrics**](AdCampaignResultsApi.md#listcampaignresultmetrics) | **GET** /v1/ads/campaign-results/metrics | List your result metrics |
| [**ListCampaignResults**](AdCampaignResultsApi.md#listcampaignresults) | **GET** /v1/ads/campaign-results | List your results per campaign |
| [**SetCampaignResultMetric**](AdCampaignResultsApi.md#setcampaignresultmetric) | **PUT** /v1/ads/campaign-results/metrics/{key} | Name a result metric |
| [**UploadCampaignResults**](AdCampaignResultsApi.md#uploadcampaignresults) | **POST** /v1/ads/campaign-results | Upload your results per campaign |

<a id="getcampaignresultsupload"></a>
# **GetCampaignResultsUpload**
> GetCampaignResultsUpload200Response GetCampaignResultsUpload (string uploadId)

Check a results upload

How an upload was matched: rows matched and unmatched, and up to 100 unmatched rows with why (`no_campaign` or `ambiguous`).  `status` turns `done` once every row is processed, usually within seconds. Uploads are kept for 30 days. 

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
    public class GetCampaignResultsUploadExample
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
            var apiInstance = new AdCampaignResultsApi(httpClient, config, httpClientHandler);
            var uploadId = "uploadId_example";  // string | 

            try
            {
                // Check a results upload
                GetCampaignResultsUpload200Response result = apiInstance.GetCampaignResultsUpload(uploadId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignResultsApi.GetCampaignResultsUpload: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignResultsUploadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check a results upload
    ApiResponse<GetCampaignResultsUpload200Response> response = apiInstance.GetCampaignResultsUploadWithHttpInfo(uploadId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignResultsApi.GetCampaignResultsUploadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **uploadId** | **string** |  |  |

### Return type

[**GetCampaignResultsUpload200Response**](GetCampaignResultsUpload200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The upload&#39;s outcome. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignresultmetrics"></a>
# **ListCampaignResultMetrics**
> ListCampaignResultMetrics200Response ListCampaignResultMetrics ()

List your result metrics

The metric keys your team has sent, with their label and kind. A new key appears as a `count` labelled from the key; name it with `PUT /v1/ads/campaign-results/metrics/{key}`. 

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
    public class ListCampaignResultMetricsExample
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
            var apiInstance = new AdCampaignResultsApi(httpClient, config, httpClientHandler);

            try
            {
                // List your result metrics
                ListCampaignResultMetrics200Response result = apiInstance.ListCampaignResultMetrics();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignResultsApi.ListCampaignResultMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignResultMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List your result metrics
    ApiResponse<ListCampaignResultMetrics200Response> response = apiInstance.ListCampaignResultMetricsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignResultsApi.ListCampaignResultMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListCampaignResultMetrics200Response**](ListCampaignResultMetrics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The metrics. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignresults"></a>
# **ListCampaignResults**
> ListCampaignResults200Response ListCampaignResults (DateOnly fromDate, DateOnly toDate, string? campaignIds = null, int? limit = null, string? cursor = null)

List your results per campaign

Your results summed per campaign over a date range, one entry per campaign with every metric it has, for the ad accounts your key can see. Each day counts its newest value only.  Paginated by campaign: pass `nextCursor` back as `cursor` until it is null. 

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
    public class ListCampaignResultsExample
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
            var apiInstance = new AdCampaignResultsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly | Inclusive. At most 400 days after `fromDate`.
            var campaignIds = "campaignIds_example";  // string? | Comma-separated platform campaign ids, at most 500. Omit for all campaigns. (optional) 
            var limit = 100;  // int? | Campaigns per page. (optional)  (default to 100)
            var cursor = "cursor_example";  // string? | `nextCursor` from the previous page. (optional) 

            try
            {
                // List your results per campaign
                ListCampaignResults200Response result = apiInstance.ListCampaignResults(fromDate, toDate, campaignIds, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignResultsApi.ListCampaignResults: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignResultsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List your results per campaign
    ApiResponse<ListCampaignResults200Response> response = apiInstance.ListCampaignResultsWithHttpInfo(fromDate, toDate, campaignIds, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignResultsApi.ListCampaignResultsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly** | Inclusive. At most 400 days after &#x60;fromDate&#x60;. |  |
| **campaignIds** | **string?** | Comma-separated platform campaign ids, at most 500. Omit for all campaigns. | [optional]  |
| **limit** | **int?** | Campaigns per page. | [optional] [default to 100] |
| **cursor** | **string?** | &#x60;nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListCampaignResults200Response**](ListCampaignResults200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One page of campaigns. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setcampaignresultmetric"></a>
# **SetCampaignResultMetric**
> SetCampaignResultMetric200Response SetCampaignResultMetric (string key, SetCampaignResultMetricRequest setCampaignResultMetricRequest)

Name a result metric

Sets a metric key's label and kind: `count` for things you count (leads, sales) or `money` with its currency (revenue). 

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
    public class SetCampaignResultMetricExample
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
            var apiInstance = new AdCampaignResultsApi(httpClient, config, httpClientHandler);
            var key = "key_example";  // string | 
            var setCampaignResultMetricRequest = new SetCampaignResultMetricRequest(); // SetCampaignResultMetricRequest | 

            try
            {
                // Name a result metric
                SetCampaignResultMetric200Response result = apiInstance.SetCampaignResultMetric(key, setCampaignResultMetricRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignResultsApi.SetCampaignResultMetric: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetCampaignResultMetricWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Name a result metric
    ApiResponse<SetCampaignResultMetric200Response> response = apiInstance.SetCampaignResultMetricWithHttpInfo(key, setCampaignResultMetricRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignResultsApi.SetCampaignResultMetricWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **key** | **string** |  |  |
| **setCampaignResultMetricRequest** | [**SetCampaignResultMetricRequest**](SetCampaignResultMetricRequest.md) |  |  |

### Return type

[**SetCampaignResultMetric200Response**](SetCampaignResultMetric200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The metric. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadcampaignresults"></a>
# **UploadCampaignResults**
> UploadCampaignResults202Response UploadCampaignResults (UploadCampaignResultsRequest uploadCampaignResultsRequest, string? idempotencyKey = null)

Upload your results per campaign

Sends your own daily numbers per campaign (qualified leads, sales, revenue...) so rules and reports can use them next to spend.  Name each row's campaign by `campaignId`, `utmCampaign` or `campaignName`. Rows are matched in the background: the `202` returns an `uploadId`, and `Location` points to `GET /v1/ads/campaign-results/uploads/{uploadId}`.  Re-sending a day replaces it. Send an `Idempotency-Key` to retry safely. Limits per team: 60 requests and 20,000 rows per hour, 512 KB per request. 

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
    public class UploadCampaignResultsExample
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
            var apiInstance = new AdCampaignResultsApi(httpClient, config, httpClientHandler);
            var uploadCampaignResultsRequest = new UploadCampaignResultsRequest(); // UploadCampaignResultsRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | A retry with the same key and body replays the first response instead of uploading twice. (optional) 

            try
            {
                // Upload your results per campaign
                UploadCampaignResults202Response result = apiInstance.UploadCampaignResults(uploadCampaignResultsRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignResultsApi.UploadCampaignResults: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadCampaignResultsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload your results per campaign
    ApiResponse<UploadCampaignResults202Response> response = apiInstance.UploadCampaignResultsWithHttpInfo(uploadCampaignResultsRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignResultsApi.UploadCampaignResultsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **uploadCampaignResultsRequest** | [**UploadCampaignResultsRequest**](UploadCampaignResultsRequest.md) |  |  |
| **idempotencyKey** | **string?** | A retry with the same key and body replays the first response instead of uploading twice. | [optional]  |

### Return type

[**UploadCampaignResults202Response**](UploadCampaignResults202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Queued for matching. |  * Location - The upload, to check how its rows were matched. <br>  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Code &#x60;ads_addon_required&#x60; when the team has no ads access. |  -  |
| **409** | The same &#x60;Idempotency-Key&#x60; is still being processed. Retry shortly. |  -  |
| **413** | Code &#x60;payload_too_large&#x60;: the body is over 512 KB. |  -  |
| **422** | The &#x60;Idempotency-Key&#x60; was used with a different body. |  -  |
| **429** | The connected account&#39;s upstream platform quota is exhausted. Behavior per platform:  - **Reddit:** rate-limits per connected Reddit user (1000 requests per 10-minute window), shared by every operation on that account. Retry after the window resets; repeated calls while exhausted do not succeed and keep the budget spent. - **Google Ads:** writes and reports run on one developer token shared by every Google Ads account on Zernio. It holds Standard access (no daily operations cap), so this only happens when Google throttles the token or your ad account. - **Google Ads envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60; (&#x60;ACCOUNT&#x60; when it is your own ad account&#39;s quota), &#x60;details.resetsAt&#x60; (ISO instant when Google accepts requests again) and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **YouTube Analytics:** reads (channel-insights, demographics, daily-views, video-retention) use the \&quot;Queries per day\&quot; quota of the Google Cloud project the account is connected through, shared with other Zernio customers, so a 429 is not your own volume. Resets at midnight Pacific Time. - **YouTube Analytics envelope:** &#x60;code: rate_limited&#x60;, &#x60;platform: google&#x60;, &#x60;details.quotaExhausted: true&#x60;, &#x60;details.quotaScope: DEVELOPER&#x60;, &#x60;details.resetsAt&#x60; and &#x60;Retry-After&#x60; counting down to it. Retrying earlier cannot succeed. - **Meta ads:** every Meta throttle (codes 4, 17, 32, 613 and business-use-case codes 80000-80014) returns 429 &#x60;rate_limited&#x60;, even when Meta answers HTTP 400. &#x60;Retry-After&#x60; comes from Meta&#39;s &#x60;x-business-use-case-usage&#x60; estimate when sent, else Meta&#39;s 60-second minimum (30 seconds for the one-write-per-30-seconds limit on one object). - **Pinterest ads:** limits per user and app, per category (ads_read, ads_write, ads_analytics). &#x60;Retry-After&#x60; comes from Pinterest&#39;s &#x60;x-ratelimit-reset&#x60; when sent, otherwise 60 seconds. - **TikTok ads:** limits per app and per endpoint (per second, minute and day), answering overage with code 40100 or code 40002 &#x60;OVER_QPS_LIMIT&#x60;. Both return 429 &#x60;rate_limited&#x60; with &#x60;platform: tiktok&#x60; and &#x60;Retry-After: 10&#x60;. Space out bulk reads (e.g. one ad at a time per advertiser) instead of retrying at once.  **TikTok Smart+ review read** (&#x60;GET /v1/ads/{adId}/tiktok-smart-plus-review&#x60;) has its own stricter TikTok quota. After an overage, Zernio answers 429 for that advertiser and connection without calling TikTok for about 60 seconds, then 120, up to 240 while TikTok keeps refusing, each with up to 10% random jitter.  A successful call holds nothing back; the next overage pauses about 60 seconds again. &#x60;Retry-After&#x60; is the time left. The advertiser-wide read (&#x60;GET /v1/ads/tiktok-smart-plus-reviews&#x60;) answers 200 with &#x60;retryAfterSeconds&#x60; and &#x60;refreshState&#x60; instead. Keep one request in flight per advertiser there.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

