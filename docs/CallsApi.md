# Zernio.Api.CallsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCall**](CallsApi.md#getcall) | **GET** /v1/calls/{id} | Get a call (any channel) |
| [**GetCallRecording**](CallsApi.md#getcallrecording) | **GET** /v1/calls/{id}/recording | Get a call recording |
| [**ListCalls**](CallsApi.md#listcalls) | **GET** /v1/calls | List all calls (unified history) |

<a id="getcall"></a>
# **GetCall**
> GetCall200Response GetCall (string id)

Get a call (any channel)

Channel-agnostic call detail: works for both WhatsApp and regular phone (PSTN) calls, so any row from `GET /v1/calls` can be opened without branching on `channel`. Returns the full call including transcript segments, with `contactId`/`contactName` set when the counterparty matches a CRM contact. 

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
    public class GetCallExample
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
            var apiInstance = new CallsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get a call (any channel)
                GetCall200Response result = apiInstance.GetCall(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CallsApi.GetCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a call (any channel)
    ApiResponse<GetCall200Response> response = apiInstance.GetCallWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CallsApi.GetCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**GetCall200Response**](GetCall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Call |  -  |
| **401** | Unauthorized |  -  |
| **403** | Not enrolled in the calling beta |  -  |
| **404** | Call not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcallrecording"></a>
# **GetCallRecording**
> GetWhatsAppCallRecording200Response GetCallRecording (string id, string? varAs = null)

Get a call recording

Channel-agnostic recording fetch: resolves a fresh, playable MP3 URL for any call regardless of channel (provider-signed URLs expire ~10 minutes after signing, so this re-signs on demand). Default responds `302 Found` redirecting to the fresh URL; pass `as=json` to receive `{ url }` instead. 

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
    public class GetCallRecordingExample
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
            var apiInstance = new CallsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var varAs = "json";  // string? | `json` returns `{ url }` instead of a 302 redirect. (optional) 

            try
            {
                // Get a call recording
                GetWhatsAppCallRecording200Response result = apiInstance.GetCallRecording(id, varAs);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CallsApi.GetCallRecording: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCallRecordingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a call recording
    ApiResponse<GetWhatsAppCallRecording200Response> response = apiInstance.GetCallRecordingWithHttpInfo(id, varAs);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CallsApi.GetCallRecordingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **varAs** | **string?** | &#x60;json&#x60; returns &#x60;{ url }&#x60; instead of a 302 redirect. | [optional]  |

### Return type

[**GetWhatsAppCallRecording200Response**](GetWhatsAppCallRecording200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **302** | Redirect to a freshly-signed recording URL. |  -  |
| **200** | Recording URL (&#x60;as&#x3D;json&#x60; only). |  -  |
| **401** | Unauthorized |  -  |
| **403** | Not enrolled in the calling beta |  -  |
| **404** | Call not found, or no recording is available for this call |  -  |
| **502** | Recording provider lookup failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcalls"></a>
# **ListCalls**
> ListCalls200Response ListCalls (string? channel = null, string? status = null, string? direction = null, string? number = null, string? search = null, DateTime? before = null, int? limit = null)

List all calls (unified history)

Unified call history across ALL of your numbers: both channels (WhatsApp Business Calling + regular phone/PSTN), inbound and outbound, newest first. Unlike `GET /v1/voice/calls` (PSTN-only) and `GET /v1/whatsapp/calls` (one account at a time), this endpoint needs no `accountId` and never requires fanning out one request per number.  Any row can be opened channel-agnostically via `GET /v1/calls/{id}` and `GET /v1/calls/{id}/recording`; no branching on `channel` needed. When the counterparty number matches a CRM contact, `contactId` and `contactName` are set.  Cursor pagination: pass the returned `nextCursor` as `before` to fetch the next page. `nextCursor` is null on the last page. 

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
    public class ListCallsExample
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
            var apiInstance = new CallsApi(httpClient, config, httpClientHandler);
            var channel = "whatsapp";  // string? |  (optional) 
            var status = "ringing";  // string? |  (optional) 
            var direction = "inbound";  // string? |  (optional) 
            var number = "number_example";  // string? | Exact filter: calls involving this number (typically one of YOUR numbers, to scope history to a single line). E.164, leading + optional. (optional) 
            var search = "search_example";  // string? | Free-text match on the from/to numbers. Non-digits are stripped, so partial queries like `302` or `+1 302` work. (optional) 
            var before = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Return calls with startedAt strictly before this instant (use the previous page's nextCursor). (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // List all calls (unified history)
                ListCalls200Response result = apiInstance.ListCalls(channel, status, direction, number, search, before, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CallsApi.ListCalls: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCallsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List all calls (unified history)
    ApiResponse<ListCalls200Response> response = apiInstance.ListCallsWithHttpInfo(channel, status, direction, number, search, before, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CallsApi.ListCallsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **channel** | **string?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |
| **direction** | **string?** |  | [optional]  |
| **number** | **string?** | Exact filter: calls involving this number (typically one of YOUR numbers, to scope history to a single line). E.164, leading + optional. | [optional]  |
| **search** | **string?** | Free-text match on the from/to numbers. Non-digits are stripped, so partial queries like &#x60;302&#x60; or &#x60;+1 302&#x60; work. | [optional]  |
| **before** | **DateTime?** | Return calls with startedAt strictly before this instant (use the previous page&#39;s nextCursor). | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |

### Return type

[**ListCalls200Response**](ListCalls200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calls, newest first |  -  |
| **401** | Unauthorized |  -  |
| **403** | Not enrolled in the calling beta |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

