# Zernio.Api.WhatsAppSandboxApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateWhatsAppSandboxSession**](WhatsAppSandboxApi.md#createwhatsappsandboxsession) | **POST** /v1/whatsapp/sandbox/sessions | Start a sandbox activation |
| [**DeleteWhatsAppSandboxSession**](WhatsAppSandboxApi.md#deletewhatsappsandboxsession) | **DELETE** /v1/whatsapp/sandbox/sessions/{sessionId} | Revoke a sandbox session |
| [**ListWhatsAppSandboxSessions**](WhatsAppSandboxApi.md#listwhatsappsandboxsessions) | **GET** /v1/whatsapp/sandbox/sessions | List your sandbox sessions |

<a id="createwhatsappsandboxsession"></a>
# **CreateWhatsAppSandboxSession**
> CreateWhatsAppSandboxSession200Response CreateWhatsAppSandboxSession (CreateWhatsAppSandboxSessionRequest createWhatsAppSandboxSessionRequest)

Start a sandbox activation

Creates (or refreshes) a pending sandbox session for the given phone and immediately fires the verified sandbox template from the shared sandbox number to that phone. The session activates when the phone owner replies to that WhatsApp message — the reply itself is proof of ownership.  One phone per user: if the caller already has a non-expired session for a DIFFERENT phone, the request is rejected with `invalid_field_value` (the message names the existing phone so it can be revoked first). Re-creating a session for the SAME phone is idempotent and refreshes the verification template.  If Meta rejects the template send (not a WhatsApp number, paused WABA, token issue), the pending row is rolled back and the Meta error message is returned in `error` so the caller knows why. 

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
    public class CreateWhatsAppSandboxSessionExample
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
            var apiInstance = new WhatsAppSandboxApi(httpClient, config, httpClientHandler);
            var createWhatsAppSandboxSessionRequest = new CreateWhatsAppSandboxSessionRequest(); // CreateWhatsAppSandboxSessionRequest | 

            try
            {
                // Start a sandbox activation
                CreateWhatsAppSandboxSession200Response result = apiInstance.CreateWhatsAppSandboxSession(createWhatsAppSandboxSessionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppSandboxApi.CreateWhatsAppSandboxSession: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWhatsAppSandboxSessionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start a sandbox activation
    ApiResponse<CreateWhatsAppSandboxSession200Response> response = apiInstance.CreateWhatsAppSandboxSessionWithHttpInfo(createWhatsAppSandboxSessionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppSandboxApi.CreateWhatsAppSandboxSessionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createWhatsAppSandboxSessionRequest** | [**CreateWhatsAppSandboxSessionRequest**](CreateWhatsAppSandboxSessionRequest.md) |  |  |

### Return type

[**CreateWhatsAppSandboxSession200Response**](CreateWhatsAppSandboxSession200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Session created or refreshed; verification template sent |  -  |
| **400** | Returned when (a) phone format is invalid, (b) phone equals the sandbox number itself, (c) the user already has a session for a different phone, or (d) Meta rejected the template send. The &#x60;error&#x60; field contains the specific reason; &#x60;param&#x60; is set when a field is at fault.  |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox addon required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletewhatsappsandboxsession"></a>
# **DeleteWhatsAppSandboxSession**
> UpdateYoutubeDefaultPlaylist200Response DeleteWhatsAppSandboxSession (string sessionId)

Revoke a sandbox session

Hard-deletes the session. The user loses the ability to send to that phone via the sandbox until they re-activate it. Existing conversations and messages already exchanged with that phone are untouched — revocation only blocks FUTURE sends.  Sessions belonging to other users cannot be revoked; the response is the same 400 as \"session not found\" so existence isn't leaked. 

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
    public class DeleteWhatsAppSandboxSessionExample
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
            var apiInstance = new WhatsAppSandboxApi(httpClient, config, httpClientHandler);
            var sessionId = "sessionId_example";  // string | The session id returned by POST /v1/whatsapp/sandbox/sessions.

            try
            {
                // Revoke a sandbox session
                UpdateYoutubeDefaultPlaylist200Response result = apiInstance.DeleteWhatsAppSandboxSession(sessionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppSandboxApi.DeleteWhatsAppSandboxSession: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWhatsAppSandboxSessionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Revoke a sandbox session
    ApiResponse<UpdateYoutubeDefaultPlaylist200Response> response = apiInstance.DeleteWhatsAppSandboxSessionWithHttpInfo(sessionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppSandboxApi.DeleteWhatsAppSandboxSessionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sessionId** | **string** | The session id returned by POST /v1/whatsapp/sandbox/sessions. |  |

### Return type

[**UpdateYoutubeDefaultPlaylist200Response**](UpdateYoutubeDefaultPlaylist200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Session revoked |  -  |
| **400** | Invalid or unknown session id |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox addon required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listwhatsappsandboxsessions"></a>
# **ListWhatsAppSandboxSessions**
> ListWhatsAppSandboxSessions200Response ListWhatsAppSandboxSessions ()

List your sandbox sessions

Returns all of the authenticated user's non-expired sandbox sessions (pending + active) plus the sandbox phone number. In practice there is at most one session per user since the sandbox is one-phone-per-user; the array shape is preserved for forward compatibility. 

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
    public class ListWhatsAppSandboxSessionsExample
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
            var apiInstance = new WhatsAppSandboxApi(httpClient, config, httpClientHandler);

            try
            {
                // List your sandbox sessions
                ListWhatsAppSandboxSessions200Response result = apiInstance.ListWhatsAppSandboxSessions();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppSandboxApi.ListWhatsAppSandboxSessions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWhatsAppSandboxSessionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List your sandbox sessions
    ApiResponse<ListWhatsAppSandboxSessions200Response> response = apiInstance.ListWhatsAppSandboxSessionsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppSandboxApi.ListWhatsAppSandboxSessionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListWhatsAppSandboxSessions200Response**](ListWhatsAppSandboxSessions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sessions retrieved successfully |  -  |
| **401** | Unauthorized |  -  |
| **403** | Inbox addon required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

