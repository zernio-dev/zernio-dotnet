# Zernio.Api.AdInsightsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAdInsightsReport**](AdInsightsApi.md#createadinsightsreport) | **POST** /v1/ads/insights/reports | Submit an async insights report run |
| [**GetAdAnalytics**](AdInsightsApi.md#getadanalytics) | **GET** /v1/ads/{adId}/analytics | Get ad analytics |
| [**GetAdInsightsReport**](AdInsightsApi.md#getadinsightsreport) | **GET** /v1/ads/insights/reports/{reportRunId} | Poll an async insights report run |
| [**GetCampaignAnalytics**](AdInsightsApi.md#getcampaignanalytics) | **GET** /v1/ads/campaigns/{campaignId}/analytics | Get campaign analytics |
| [**QueryAdInsights**](AdInsightsApi.md#queryadinsights) | **GET** /v1/ads/insights | Flexible live insights query |

<a id="createadinsightsreport"></a>
# **CreateAdInsightsReport**
> CreateAdInsightsReport202Response CreateAdInsightsReport (CreateAdInsightsReportRequest createAdInsightsReportRequest)

Submit an async insights report run

Submits an asynchronous Meta insights report. Same query surface as GET /v1/ads/insights, but in the JSON body; Meta processes the report server-side, which is the right choice for long ranges or large accounts where the sync query is slow or rate-limited. Returns a `reportRunId` to poll via GET /v1/ads/insights/reports/{reportRunId}. 

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
    public class CreateAdInsightsReportExample
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
            var apiInstance = new AdInsightsApi(httpClient, config, httpClientHandler);
            var createAdInsightsReportRequest = new CreateAdInsightsReportRequest(); // CreateAdInsightsReportRequest | 

            try
            {
                // Submit an async insights report run
                CreateAdInsightsReport202Response result = apiInstance.CreateAdInsightsReport(createAdInsightsReportRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdInsightsApi.CreateAdInsightsReport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdInsightsReportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit an async insights report run
    ApiResponse<CreateAdInsightsReport202Response> response = apiInstance.CreateAdInsightsReportWithHttpInfo(createAdInsightsReportRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdInsightsApi.CreateAdInsightsReportWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdInsightsReportRequest** | [**CreateAdInsightsReportRequest**](CreateAdInsightsReportRequest.md) |  |  |

### Return type

[**CreateAdInsightsReport202Response**](CreateAdInsightsReport202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Report run submitted |  -  |
| **400** | Invalid input, or Meta rejected the report parameters |  -  |
| **401** | Unauthorized |  -  |
| **429** | Meta rate limit reached |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadanalytics"></a>
# **GetAdAnalytics**
> GetAdAnalytics200Response GetAdAnalytics (string adId, DateOnly? fromDate = null, DateOnly? toDate = null, string? breakdowns = null)

Get ad analytics

Returns detailed performance analytics for an ad. Includes summary metrics, a daily timeline over the requested date range, and optional demographic breakdowns (Meta and TikTok only). If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max. 

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
    public class GetAdAnalyticsExample
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
            var apiInstance = new AdInsightsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 
            var breakdowns = "breakdowns_example";  // string? | Comma-separated breakdown dimensions.  **Meta**: age, gender, country, publisher_platform, device_platform, region.  **TikTok**: gender, age, country_code, platform, ac, language.  **LinkedIn** (firmographics): job_title, job_function, seniority, industry, company, company_size, country, region. Rows carry the raw pivot `value` plus a resolved `name`. LinkedIn serves these aggregated over the whole range, delays the data 12-24h, and omits segments with fewer than 3 events.  (optional) 

            try
            {
                // Get ad analytics
                GetAdAnalytics200Response result = apiInstance.GetAdAnalytics(adId, fromDate, toDate, breakdowns);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdInsightsApi.GetAdAnalytics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdAnalyticsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ad analytics
    ApiResponse<GetAdAnalytics200Response> response = apiInstance.GetAdAnalyticsWithHttpInfo(adId, fromDate, toDate, breakdowns);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdInsightsApi.GetAdAnalyticsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** |  |  |
| **fromDate** | **DateOnly?** | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |
| **breakdowns** | **string?** | Comma-separated breakdown dimensions.  **Meta**: age, gender, country, publisher_platform, device_platform, region.  **TikTok**: gender, age, country_code, platform, ac, language.  **LinkedIn** (firmographics): job_title, job_function, seniority, industry, company, company_size, country, region. Rows carry the raw pivot &#x60;value&#x60; plus a resolved &#x60;name&#x60;. LinkedIn serves these aggregated over the whole range, delays the data 12-24h, and omits segments with fewer than 3 events.  | [optional]  |

### Return type

[**GetAdAnalytics200Response**](GetAdAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad analytics |  -  |
| **202** | Part of the requested date range predates the ingested history; a background backfill job has been queued. The body has the same shape as the 200 response, carries the currently-available data, and includes &#x60;backfillPending: true&#x60;. A &#x60;Retry-After&#x60; header carries the recommended poll interval in seconds. Allow the job a short time to run (typically 1-3 minutes) and submit the request again; once ingestion completes the same request returns 200 with the full range. |  -  |
| **400** | Invalid parameter (e.g. an unknown &#x60;breakdowns&#x60; dimension). The message lists the offending value(s) and the supported set. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadinsightsreport"></a>
# **GetAdInsightsReport**
> GetAdInsightsReport200Response GetAdInsightsReport (string reportRunId, string accountId, int? limit = null, string? after = null)

Poll an async insights report run

Status and results for a report run created via POST /v1/ads/insights/reports. While the job runs, returns `status` and `percentCompletion`. Once `status` is \"Job Completed\" the response also carries a `data` page, cursor-paginated via `limit` / `after`. 

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
    public class GetAdInsightsReportExample
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
            var apiInstance = new AdInsightsApi(httpClient, config, httpClientHandler);
            var reportRunId = "reportRunId_example";  // string | 
            var accountId = "accountId_example";  // string | Zernio SocialAccount id used to resolve the Meta token (must be the same connection that created the run).
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string? |  (optional) 

            try
            {
                // Poll an async insights report run
                GetAdInsightsReport200Response result = apiInstance.GetAdInsightsReport(reportRunId, accountId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdInsightsApi.GetAdInsightsReport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdInsightsReportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Poll an async insights report run
    ApiResponse<GetAdInsightsReport200Response> response = apiInstance.GetAdInsightsReportWithHttpInfo(reportRunId, accountId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdInsightsApi.GetAdInsightsReportWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **reportRunId** | **string** |  |  |
| **accountId** | **string** | Zernio SocialAccount id used to resolve the Meta token (must be the same connection that created the run). |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string?** |  | [optional]  |

### Return type

[**GetAdInsightsReport200Response**](GetAdInsightsReport200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Report run status (plus results when completed) |  -  |
| **400** | Invalid input, or the report run is not readable with this account&#39;s token |  -  |
| **401** | Unauthorized |  -  |
| **429** | Meta rate limit reached |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignanalytics"></a>
# **GetCampaignAnalytics**
> GetCampaignAnalytics200Response GetCampaignAnalytics (string campaignId, string? platform = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? breakdowns = null)

Get campaign analytics

Returns performance analytics for a whole campaign in one call: summary metrics, a daily timeline over the requested date range (summed across the campaign's ads), and optional demographic breakdowns. Breakdowns are fetched live from Meta at the campaign level (one call per dimension, no per-ad fan-out), so an agency dashboard gets campaign-level age/gender/etc. without summing thousands of per-ad reads. `campaignId` is the platform campaign id; pass `platform` when a campaign id could be ambiguous across platforms. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max. 

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
    public class GetCampaignAnalyticsExample
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
            var apiInstance = new AdInsightsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Platform campaign id (platformCampaignId).
            var platform = "platform_example";  // string? | Disambiguate when the campaign id exists across platforms (e.g. facebook, instagram). (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 
            var breakdowns = "breakdowns_example";  // string? | Comma-separated breakdown dimensions.  **Meta**: age, gender, country, publisher_platform, device_platform, region, platform_position, impression_device, video_asset, image_asset, body_asset, title_asset.  **LinkedIn** (firmographics): job_title, job_function, seniority, industry, company, company_size, country, region. Rows carry the raw pivot `value` plus a resolved `name`. LinkedIn serves these aggregated over the whole range, delays the data 12-24h, and omits segments with fewer than 3 events.  (optional) 

            try
            {
                // Get campaign analytics
                GetCampaignAnalytics200Response result = apiInstance.GetCampaignAnalytics(campaignId, platform, fromDate, toDate, breakdowns);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdInsightsApi.GetCampaignAnalytics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignAnalyticsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get campaign analytics
    ApiResponse<GetCampaignAnalytics200Response> response = apiInstance.GetCampaignAnalyticsWithHttpInfo(campaignId, platform, fromDate, toDate, breakdowns);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdInsightsApi.GetCampaignAnalyticsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Platform campaign id (platformCampaignId). |  |
| **platform** | **string?** | Disambiguate when the campaign id exists across platforms (e.g. facebook, instagram). | [optional]  |
| **fromDate** | **DateOnly?** | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |
| **breakdowns** | **string?** | Comma-separated breakdown dimensions.  **Meta**: age, gender, country, publisher_platform, device_platform, region, platform_position, impression_device, video_asset, image_asset, body_asset, title_asset.  **LinkedIn** (firmographics): job_title, job_function, seniority, industry, company, company_size, country, region. Rows carry the raw pivot &#x60;value&#x60; plus a resolved &#x60;name&#x60;. LinkedIn serves these aggregated over the whole range, delays the data 12-24h, and omits segments with fewer than 3 events.  | [optional]  |

### Return type

[**GetCampaignAnalytics200Response**](GetCampaignAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign analytics |  -  |
| **202** | Part of the requested date range predates the ingested history; a background backfill job has been queued. The body has the same shape as the 200 response, carries the currently-available data, and includes &#x60;backfillPending: true&#x60;. A &#x60;Retry-After&#x60; header carries the recommended poll interval in seconds. Allow the job a short time to run (typically 1-3 minutes) and submit the request again; once ingestion completes the same request returns 200 with the full range. |  -  |
| **400** | Invalid parameter (e.g. an unknown &#x60;breakdowns&#x60; dimension). The message lists the offending value(s) and the supported set. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="queryadinsights"></a>
# **QueryAdInsights**
> QueryAdInsights200Response QueryAdInsights (string accountId, string objectId, string? level = null, string? fields = null, string? breakdowns = null, string? actionBreakdowns = null, string? actionAttributionWindows = null, string? actionReportTime = null, bool? useUnifiedAttributionSetting = null, string? filtering = null, string? datePreset = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? timeIncrement = null, int? limit = null, string? after = null)

Flexible live insights query

Live, flexible insights query against Meta's Graph API. Unlike GET /v1/ads/{adId}/analytics (fixed metric set, cached), this forwards caller-chosen `fields`, `breakdowns` and `filtering` to any Meta insights node and returns Meta's rows verbatim.  `objectId` selects the node: an ad account, campaign, ad set or ad platform id. `level` sets row granularity independently of the node.  Semantic validation is Meta's: an unknown field or invalid breakdown combination returns a 400 carrying Meta's message. For long ranges or agency-scale accounts prefer the async variant (POST /v1/ads/insights/reports). 

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
    public class QueryAdInsightsExample
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
            var apiInstance = new AdInsightsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var objectId = "objectId_example";  // string | Meta insights node: act_<n>, campaign id, ad set id or ad id.
            var level = "ad";  // string? | Row granularity (optional) 
            var fields = "fields_example";  // string? | Comma-separated Graph insights fields (e.g. spend,impressions,frequency,website_purchase_roas). Omitted = Meta's default set. (optional) 
            var breakdowns = "breakdowns_example";  // string? | Comma-separated Graph breakdowns (e.g. age,gender or publisher_platform). (optional) 
            var actionBreakdowns = "actionBreakdowns_example";  // string? | Comma-separated Graph action breakdowns. Segments the actions[] arrays in each row. (optional) 
            var actionAttributionWindows = "actionAttributionWindows_example";  // string? | Comma-separated Meta attribution windows. Action values are returned keyed per window. (optional) 
            var actionReportTime = "actionReportTime_example";  // string? | When actions are counted: impression, conversion or mixed. (optional) 
            var useUnifiedAttributionSetting = true;  // bool? | Use the ad sets' own attribution settings for action counting. (optional) 
            var filtering = "filtering_example";  // string? | JSON array of Meta filter objects: [{\"field\", \"operator\", \"value\"}]. Applied server-side by Meta. (optional) 
            var datePreset = "datePreset_example";  // string? | Meta date_preset (e.g. last_7d, last_30d, this_month). Mutually exclusive with fromDate/toDate. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of range (YYYY-MM-DD); requires toDate. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of range (YYYY-MM-DD); requires fromDate. (optional) 
            var timeIncrement = "timeIncrement_example";  // string? | Days per row (1-90), monthly, or all_days. (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Flexible live insights query
                QueryAdInsights200Response result = apiInstance.QueryAdInsights(accountId, objectId, level, fields, breakdowns, actionBreakdowns, actionAttributionWindows, actionReportTime, useUnifiedAttributionSetting, filtering, datePreset, fromDate, toDate, timeIncrement, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdInsightsApi.QueryAdInsights: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the QueryAdInsightsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Flexible live insights query
    ApiResponse<QueryAdInsights200Response> response = apiInstance.QueryAdInsightsWithHttpInfo(accountId, objectId, level, fields, breakdowns, actionBreakdowns, actionAttributionWindows, actionReportTime, useUnifiedAttributionSetting, filtering, datePreset, fromDate, toDate, timeIncrement, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdInsightsApi.QueryAdInsightsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **objectId** | **string** | Meta insights node: act_&lt;n&gt;, campaign id, ad set id or ad id. |  |
| **level** | **string?** | Row granularity | [optional]  |
| **fields** | **string?** | Comma-separated Graph insights fields (e.g. spend,impressions,frequency,website_purchase_roas). Omitted &#x3D; Meta&#39;s default set. | [optional]  |
| **breakdowns** | **string?** | Comma-separated Graph breakdowns (e.g. age,gender or publisher_platform). | [optional]  |
| **actionBreakdowns** | **string?** | Comma-separated Graph action breakdowns. Segments the actions[] arrays in each row. | [optional]  |
| **actionAttributionWindows** | **string?** | Comma-separated Meta attribution windows. Action values are returned keyed per window. | [optional]  |
| **actionReportTime** | **string?** | When actions are counted: impression, conversion or mixed. | [optional]  |
| **useUnifiedAttributionSetting** | **bool?** | Use the ad sets&#39; own attribution settings for action counting. | [optional]  |
| **filtering** | **string?** | JSON array of Meta filter objects: [{\&quot;field\&quot;, \&quot;operator\&quot;, \&quot;value\&quot;}]. Applied server-side by Meta. | [optional]  |
| **datePreset** | **string?** | Meta date_preset (e.g. last_7d, last_30d, this_month). Mutually exclusive with fromDate/toDate. | [optional]  |
| **fromDate** | **DateOnly?** | Start of range (YYYY-MM-DD); requires toDate. | [optional]  |
| **toDate** | **DateOnly?** | End of range (YYYY-MM-DD); requires fromDate. | [optional]  |
| **timeIncrement** | **string?** | Days per row (1-90), monthly, or all_days. | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**QueryAdInsights200Response**](QueryAdInsights200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Insight rows (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query (unknown field, invalid breakdown combo) — message carries Meta&#39;s error |  -  |
| **401** | Unauthorized |  -  |
| **429** | Meta rate limit reached |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

