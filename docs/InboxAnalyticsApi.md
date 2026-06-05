# Zernio.Api.InboxAnalyticsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetInboxConversationAnalytics**](InboxAnalyticsApi.md#getinboxconversationanalytics) | **GET** /v1/analytics/inbox/conversations/{conversationId} | Get analytics for a single conversation |
| [**GetInboxHeatmap**](InboxAnalyticsApi.md#getinboxheatmap) | **GET** /v1/analytics/inbox/heatmap | Get inbox day-of-week × hour-of-day heatmap |
| [**GetInboxResponseTime**](InboxAnalyticsApi.md#getinboxresponsetime) | **GET** /v1/analytics/inbox/response-time | Get inbox response-time stats |
| [**GetInboxSourceBreakdown**](InboxAnalyticsApi.md#getinboxsourcebreakdown) | **GET** /v1/analytics/inbox/source-breakdown | Get inbox source breakdown |
| [**GetInboxTopAccounts**](InboxAnalyticsApi.md#getinboxtopaccounts) | **GET** /v1/analytics/inbox/top-accounts | Get top accounts by inbox volume |
| [**GetInboxVolume**](InboxAnalyticsApi.md#getinboxvolume) | **GET** /v1/analytics/inbox/volume | Get inbox messaging volume |
| [**ListInboxConversationAnalytics**](InboxAnalyticsApi.md#listinboxconversationanalytics) | **GET** /v1/analytics/inbox/conversations | List conversations with inbox analytics |

<a id="getinboxconversationanalytics"></a>
# **GetInboxConversationAnalytics**
> GetInboxConversationAnalytics200Response GetInboxConversationAnalytics (string conversationId, DateOnly fromDate, DateOnly? toDate = null)

Get analytics for a single conversation

Per-conversation inbox analytics. The inbox analog of /v1/analytics/post-timeline — one conversation, daily totals, source mix.  The {conversationId} path param accepts EITHER the Mongo `_id` of the Conversation document OR its `platformConversationId` (the same identity used by metadata.conversationId at ingest time). Ownership is verified in MongoDB against the caller's team before the Tinybird query fires.  Max date range is 365 days. 

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
    public class GetInboxConversationAnalyticsExample
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
            var apiInstance = new InboxAnalyticsApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | Mongo _id or platformConversationId.
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 

            try
            {
                // Get analytics for a single conversation
                GetInboxConversationAnalytics200Response result = apiInstance.GetInboxConversationAnalytics(conversationId, fromDate, toDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxConversationAnalytics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxConversationAnalyticsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get analytics for a single conversation
    ApiResponse<GetInboxConversationAnalytics200Response> response = apiInstance.GetInboxConversationAnalyticsWithHttpInfo(conversationId, fromDate, toDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxConversationAnalyticsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** | Mongo _id or platformConversationId. |  |
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly?** |  | [optional]  |

### Return type

[**GetInboxConversationAnalytics200Response**](GetInboxConversationAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-conversation analytics |  -  |
| **400** | Validation error |  -  |
| **401** | Unauthorized |  -  |
| **404** | Conversation not found or not owned by the caller&#39;s team |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxheatmap"></a>
# **GetInboxHeatmap**
> GetInboxHeatmap200Response GetInboxHeatmap (DateOnly fromDate, DateOnly? toDate = null, string? profileId = null, string? platform = null, string? accountId = null, string? source = null, string? action = null)

Get inbox day-of-week × hour-of-day heatmap

Day-of-week × hour-of-day breakdown of inbox messages. Buckets are sparse — only cells with at least one event are returned; clients zero-fill the rest to render the full 7×24 grid. The `dow` field follows ClickHouse's `toDayOfWeek` convention (1 = Monday … 7 = Sunday). Max date range is 365 days. 

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
    public class GetInboxHeatmapExample
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
            var apiInstance = new InboxAnalyticsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var profileId = "profileId_example";  // string? |  (optional) 
            var platform = "platform_example";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? |  (optional) 
            var source = "source_example";  // string? |  (optional) 
            var action = "message.received";  // string? | Narrow to a single event type. \"all\" or omitted means no filter. (optional) 

            try
            {
                // Get inbox day-of-week × hour-of-day heatmap
                GetInboxHeatmap200Response result = apiInstance.GetInboxHeatmap(fromDate, toDate, profileId, platform, accountId, source, action);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxHeatmap: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxHeatmapWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get inbox day-of-week × hour-of-day heatmap
    ApiResponse<GetInboxHeatmap200Response> response = apiInstance.GetInboxHeatmapWithHttpInfo(fromDate, toDate, profileId, platform, accountId, source, action);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxHeatmapWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly?** |  | [optional]  |
| **profileId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **accountId** | **string?** |  | [optional]  |
| **source** | **string?** |  | [optional]  |
| **action** | **string?** | Narrow to a single event type. \&quot;all\&quot; or omitted means no filter. | [optional]  |

### Return type

[**GetInboxHeatmap200Response**](GetInboxHeatmap200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Heatmap buckets |  -  |
| **400** | Validation error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxresponsetime"></a>
# **GetInboxResponseTime**
> GetInboxResponseTime200Response GetInboxResponseTime (DateOnly fromDate, DateOnly? toDate = null, string? profileId = null, string? platform = null, string? accountId = null)

Get inbox response-time stats

Time-to-first-response stats. Pairs each received message with the next sent message in the same conversation and reports the delta as both summary statistics and a fixed-bucket histogram suited for the analytics page's TTR chart.  `sampleSize` reflects only conversations that received AND got a reply in the window — received-but-never-answered conversations are excluded. Compare against /v1/analytics/inbox/volume's `summary.received` to compute reply rate.  Max date range is 365 days. 

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
    public class GetInboxResponseTimeExample
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
            var apiInstance = new InboxAnalyticsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var profileId = "profileId_example";  // string? |  (optional) 
            var platform = "platform_example";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? |  (optional) 

            try
            {
                // Get inbox response-time stats
                GetInboxResponseTime200Response result = apiInstance.GetInboxResponseTime(fromDate, toDate, profileId, platform, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxResponseTime: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxResponseTimeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get inbox response-time stats
    ApiResponse<GetInboxResponseTime200Response> response = apiInstance.GetInboxResponseTimeWithHttpInfo(fromDate, toDate, profileId, platform, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxResponseTimeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly?** |  | [optional]  |
| **profileId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **accountId** | **string?** |  | [optional]  |

### Return type

[**GetInboxResponseTime200Response**](GetInboxResponseTime200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response-time summary + histogram |  -  |
| **400** | Validation error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxsourcebreakdown"></a>
# **GetInboxSourceBreakdown**
> GetInboxSourceBreakdown200Response GetInboxSourceBreakdown (DateOnly fromDate, DateOnly? toDate = null, string? profileId = null, string? platform = null, string? accountId = null)

Get inbox source breakdown

Breakdown of inbox messages by their lineage source (the `metadata.source` field set at ingest time: human / workflow / sequence / broadcast / comment_automation / api / contact / platform). Each source row also carries a per-platform sub-split. Max date range is 365 days. 

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
    public class GetInboxSourceBreakdownExample
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
            var apiInstance = new InboxAnalyticsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var profileId = "profileId_example";  // string? |  (optional) 
            var platform = "platform_example";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? |  (optional) 

            try
            {
                // Get inbox source breakdown
                GetInboxSourceBreakdown200Response result = apiInstance.GetInboxSourceBreakdown(fromDate, toDate, profileId, platform, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxSourceBreakdown: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxSourceBreakdownWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get inbox source breakdown
    ApiResponse<GetInboxSourceBreakdown200Response> response = apiInstance.GetInboxSourceBreakdownWithHttpInfo(fromDate, toDate, profileId, platform, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxSourceBreakdownWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly?** |  | [optional]  |
| **profileId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **accountId** | **string?** |  | [optional]  |

### Return type

[**GetInboxSourceBreakdown200Response**](GetInboxSourceBreakdown200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Source breakdown |  -  |
| **400** | Validation error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxtopaccounts"></a>
# **GetInboxTopAccounts**
> GetInboxTopAccounts200Response GetInboxTopAccounts (DateOnly fromDate, DateOnly? toDate = null, string? profileId = null, string? platform = null, string? source = null, int? limit = null)

Get top accounts by inbox volume

Leaderboard of social accounts by inbox message volume. Decorates each row with display labels from the live SocialAccount record (so the UI shows username + displayName, not just an ID). Accounts that no longer map to a SocialAccount surface as \"(disconnected)\" so the row stays visible. Max date range is 365 days. 

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
    public class GetInboxTopAccountsExample
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
            var apiInstance = new InboxAnalyticsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var profileId = "profileId_example";  // string? |  (optional) 
            var platform = "platform_example";  // string? |  (optional) 
            var source = "source_example";  // string? |  (optional) 
            var limit = 10;  // int? | Cap on returned rows. Lower than the posting listing's 100 because each row triggers a SocialAccount Mongo lookup. (optional)  (default to 10)

            try
            {
                // Get top accounts by inbox volume
                GetInboxTopAccounts200Response result = apiInstance.GetInboxTopAccounts(fromDate, toDate, profileId, platform, source, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxTopAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxTopAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get top accounts by inbox volume
    ApiResponse<GetInboxTopAccounts200Response> response = apiInstance.GetInboxTopAccountsWithHttpInfo(fromDate, toDate, profileId, platform, source, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxTopAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly?** |  | [optional]  |
| **profileId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **source** | **string?** |  | [optional]  |
| **limit** | **int?** | Cap on returned rows. Lower than the posting listing&#39;s 100 because each row triggers a SocialAccount Mongo lookup. | [optional] [default to 10] |

### Return type

[**GetInboxTopAccounts200Response**](GetInboxTopAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Top accounts leaderboard |  -  |
| **400** | Validation error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getinboxvolume"></a>
# **GetInboxVolume**
> GetInboxVolume200Response GetInboxVolume (DateOnly fromDate, DateOnly? toDate = null, string? profileId = null, string? platform = null, string? accountId = null, string? source = null)

Get inbox messaging volume

Daily inbox messaging volume + breakdowns. Folds the raw messaging events into three projections so the client can render the volume chart, KPI strip, and per-platform stacked bar from a single call. Max date range is 365 days. 

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
    public class GetInboxVolumeExample
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
            var apiInstance = new InboxAnalyticsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | Inclusive lower bound (YYYY-MM-DD). Required.
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Inclusive upper bound (YYYY-MM-DD). Defaults to today. (optional) 
            var profileId = "profileId_example";  // string? |  (optional) 
            var platform = "platform_example";  // string? | Filter by single platform (facebook, instagram, twitter, etc.). (optional) 
            var accountId = "accountId_example";  // string? |  (optional) 
            var source = "source_example";  // string? | Filter by metadata.source lineage (human, workflow, sequence, broadcast, comment_automation, api, contact, platform). (optional) 

            try
            {
                // Get inbox messaging volume
                GetInboxVolume200Response result = apiInstance.GetInboxVolume(fromDate, toDate, profileId, platform, accountId, source);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxVolume: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInboxVolumeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get inbox messaging volume
    ApiResponse<GetInboxVolume200Response> response = apiInstance.GetInboxVolumeWithHttpInfo(fromDate, toDate, profileId, platform, accountId, source);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxAnalyticsApi.GetInboxVolumeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** | Inclusive lower bound (YYYY-MM-DD). Required. |  |
| **toDate** | **DateOnly?** | Inclusive upper bound (YYYY-MM-DD). Defaults to today. | [optional]  |
| **profileId** | **string?** |  | [optional]  |
| **platform** | **string?** | Filter by single platform (facebook, instagram, twitter, etc.). | [optional]  |
| **accountId** | **string?** |  | [optional]  |
| **source** | **string?** | Filter by metadata.source lineage (human, workflow, sequence, broadcast, comment_automation, api, contact, platform). | [optional]  |

### Return type

[**GetInboxVolume200Response**](GetInboxVolume200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Volume breakdown |  -  |
| **400** | Validation error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listinboxconversationanalytics"></a>
# **ListInboxConversationAnalytics**
> ListInboxConversationAnalytics200Response ListInboxConversationAnalytics (DateOnly fromDate, DateOnly? toDate = null, string? profileId = null, string? platform = null, string? accountId = null, string? source = null, int? limit = null, int? page = null, string? sortBy = null, string? order = null)

List conversations with inbox analytics

Per-conversation listing with per-row totals + first/last message timestamps. The inbox analog of GET /v1/analytics (posts listing) — same filter shape, same pagination, same sort/order semantics. Use as the entry point for the per-conversation analytics drawer at /v1/analytics/inbox/conversations/{conversationId}.  Rows are enriched with the conversation's participant info (`participantName`, `participantUsername`, `participantPicture`) and last-message preview by joining the Conversation document scoped to the caller's team. Max date range is 365 days. 

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
    public class ListInboxConversationAnalyticsExample
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
            var apiInstance = new InboxAnalyticsApi(httpClient, config, httpClientHandler);
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly | 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? |  (optional) 
            var profileId = "profileId_example";  // string? |  (optional) 
            var platform = "platform_example";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? |  (optional) 
            var source = "source_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var page = 1;  // int? |  (optional)  (default to 1)
            var sortBy = "lastMessageAt";  // string? |  (optional)  (default to lastMessageAt)
            var order = "asc";  // string? |  (optional)  (default to desc)

            try
            {
                // List conversations with inbox analytics
                ListInboxConversationAnalytics200Response result = apiInstance.ListInboxConversationAnalytics(fromDate, toDate, profileId, platform, accountId, source, limit, page, sortBy, order);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InboxAnalyticsApi.ListInboxConversationAnalytics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInboxConversationAnalyticsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List conversations with inbox analytics
    ApiResponse<ListInboxConversationAnalytics200Response> response = apiInstance.ListInboxConversationAnalyticsWithHttpInfo(fromDate, toDate, profileId, platform, accountId, source, limit, page, sortBy, order);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InboxAnalyticsApi.ListInboxConversationAnalyticsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fromDate** | **DateOnly** |  |  |
| **toDate** | **DateOnly?** |  | [optional]  |
| **profileId** | **string?** |  | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **accountId** | **string?** |  | [optional]  |
| **source** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **page** | **int?** |  | [optional] [default to 1] |
| **sortBy** | **string?** |  | [optional] [default to lastMessageAt] |
| **order** | **string?** |  | [optional] [default to desc] |

### Return type

[**ListInboxConversationAnalytics200Response**](ListInboxConversationAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated conversation analytics list |  -  |
| **400** | Validation error |  -  |
| **401** | Unauthorized |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

