# Zernio.Api.LogsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListLogs**](LogsApi.md#listlogs) | **GET** /v1/logs | List activity logs |

<a id="listlogs"></a>
# **ListLogs**
> ListLogs200Response ListLogs (string? type = null, string? status = null, string? platform = null, string? action = null, string? search = null, int? days = null, int? limit = null, int? skip = null, string? accountId = null, string? varEvent = null, string? requestId = null, DateTime? from = null, DateTime? to = null, int? statusCode = null, string? apiKeyId = null, bool? includeReadReceipts = null)

List activity logs

Unified logs endpoint. Returns logs for publishing, connections, webhooks, and messaging. Filter by type, platform, status, and time range. Logs are retained for 90 days. 

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
    public class ListLogsExample
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
            var apiInstance = new LogsApi(httpClient, config, httpClientHandler);
            var type = "all";  // string? | Log category to query. Use `all` for the unified view across every category, or `api_request` for your API request logs (method, path, status, latency).  (optional)  (default to publishing)
            var status = "success";  // string? | Filter by status (optional) 
            var platform = "tiktok";  // string? | Filter by platform (optional) 
            var action = "action_example";  // string? | Filter by action (e.g., post.published, message.sent, account.connected, webhook.delivered) (optional) 
            var search = "search_example";  // string? | Free-text search across log fields (optional) 
            var days = 90;  // int? | Number of days to look back (max 90) (optional)  (default to 90)
            var limit = 50;  // int? | Maximum number of logs to return (max 100) (optional)  (default to 50)
            var skip = 0;  // int? | Number of logs to skip (for pagination) (optional)  (default to 0)
            var accountId = "accountId_example";  // string? | Filter by connected account ID (optional) 
            var varEvent = "varEvent_example";  // string? | Filter webhook logs by event (e.g. post.published, message.received) (optional) 
            var requestId = "requestId_example";  // string? | Correlation ID — returns every log spawned by a single API request (optional) 
            var from = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Precise start instant (ISO 8601); narrows within the day range (optional) 
            var to = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Precise end instant (ISO 8601) (optional) 
            var statusCode = 56;  // int? | Filter by exact HTTP status code (api_request logs) (optional) 
            var apiKeyId = "apiKeyId_example";  // string? | Filter by the API key that made the request (api_request logs) (optional) 
            var includeReadReceipts = false;  // bool? | Include message.read / message.delivered events (hidden by default for messaging logs) (optional)  (default to false)

            try
            {
                // List activity logs
                ListLogs200Response result = apiInstance.ListLogs(type, status, platform, action, search, days, limit, skip, accountId, varEvent, requestId, from, to, statusCode, apiKeyId, includeReadReceipts);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LogsApi.ListLogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List activity logs
    ApiResponse<ListLogs200Response> response = apiInstance.ListLogsWithHttpInfo(type, status, platform, action, search, days, limit, skip, accountId, varEvent, requestId, from, to, statusCode, apiKeyId, includeReadReceipts);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LogsApi.ListLogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **type** | **string?** | Log category to query. Use &#x60;all&#x60; for the unified view across every category, or &#x60;api_request&#x60; for your API request logs (method, path, status, latency).  | [optional] [default to publishing] |
| **status** | **string?** | Filter by status | [optional]  |
| **platform** | **string?** | Filter by platform | [optional]  |
| **action** | **string?** | Filter by action (e.g., post.published, message.sent, account.connected, webhook.delivered) | [optional]  |
| **search** | **string?** | Free-text search across log fields | [optional]  |
| **days** | **int?** | Number of days to look back (max 90) | [optional] [default to 90] |
| **limit** | **int?** | Maximum number of logs to return (max 100) | [optional] [default to 50] |
| **skip** | **int?** | Number of logs to skip (for pagination) | [optional] [default to 0] |
| **accountId** | **string?** | Filter by connected account ID | [optional]  |
| **varEvent** | **string?** | Filter webhook logs by event (e.g. post.published, message.received) | [optional]  |
| **requestId** | **string?** | Correlation ID — returns every log spawned by a single API request | [optional]  |
| **from** | **DateTime?** | Precise start instant (ISO 8601); narrows within the day range | [optional]  |
| **to** | **DateTime?** | Precise end instant (ISO 8601) | [optional]  |
| **statusCode** | **int?** | Filter by exact HTTP status code (api_request logs) | [optional]  |
| **apiKeyId** | **string?** | Filter by the API key that made the request (api_request logs) | [optional]  |
| **includeReadReceipts** | **bool?** | Include message.read / message.delivered events (hidden by default for messaging logs) | [optional] [default to false] |

### Return type

[**ListLogs200Response**](ListLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Logs retrieved successfully |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

