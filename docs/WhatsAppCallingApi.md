# Zernio.Api.WhatsAppCallingApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DisableWhatsAppCalling**](WhatsAppCallingApi.md#disablewhatsappcalling) | **DELETE** /v1/whatsapp/phone-numbers/{id}/calling | Disable calling on a number |
| [**EnableWhatsAppCalling**](WhatsAppCallingApi.md#enablewhatsappcalling) | **POST** /v1/whatsapp/phone-numbers/{id}/calling | Enable calling on a number |
| [**GetWhatsAppCall**](WhatsAppCallingApi.md#getwhatsappcall) | **GET** /v1/whatsapp/calls/{callId} | Get a single call |
| [**GetWhatsAppCallEstimate**](WhatsAppCallingApi.md#getwhatsappcallestimate) | **GET** /v1/whatsapp/calls/estimate | Estimate per-minute cost for a destination |
| [**GetWhatsAppCallPermissions**](WhatsAppCallingApi.md#getwhatsappcallpermissions) | **GET** /v1/whatsapp/call-permissions | Check call permission for a consumer |
| [**GetWhatsAppCallingConfig**](WhatsAppCallingApi.md#getwhatsappcallingconfig) | **GET** /v1/whatsapp/calling | Get calling config for an account |
| [**InitiateWhatsAppCall**](WhatsAppCallingApi.md#initiatewhatsappcall) | **POST** /v1/whatsapp/calls | Initiate outbound call |
| [**ListWhatsAppCalls**](WhatsAppCallingApi.md#listwhatsappcalls) | **GET** /v1/whatsapp/calls | List call history for an account |
| [**UpdateWhatsAppCalling**](WhatsAppCallingApi.md#updatewhatsappcalling) | **PATCH** /v1/whatsapp/phone-numbers/{id}/calling | Update calling config |

<a id="disablewhatsappcalling"></a>
# **DisableWhatsAppCalling**
> void DisableWhatsAppCalling (string id, string accountId)

Disable calling on a number

Disable calling. Sends calling.status=DISABLED to Meta (best-effort) and flips the local `callingEnabled` flag off. forwardTo and SIP creds are preserved so a re-enable does not lose the destination. 

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
    public class DisableWhatsAppCallingExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Disable calling on a number
                apiInstance.DisableWhatsAppCalling(id, accountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.DisableWhatsAppCalling: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisableWhatsAppCallingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Disable calling on a number
    apiInstance.DisableWhatsAppCallingWithHttpInfo(id, accountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.DisableWhatsAppCallingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Disabled |  -  |
| **401** | Unauthorized |  -  |
| **404** | WhatsApp phone number not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="enablewhatsappcalling"></a>
# **EnableWhatsAppCalling**
> EnableWhatsAppCalling200Response EnableWhatsAppCalling (string id, EnableWhatsAppCallingRequest enableWhatsAppCallingRequest)

Enable calling on a number

Enable WhatsApp Business Calling on a connected number. Configures Meta calling.status=ENABLED with our Telnyx SIP endpoint, fetches and stores the Meta-issued SIP password (encrypted), and snapshots the customer's forward-to destination. 

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
    public class EnableWhatsAppCallingExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | WhatsAppPhoneNumber Mongo ID
            var enableWhatsAppCallingRequest = new EnableWhatsAppCallingRequest(); // EnableWhatsAppCallingRequest | 

            try
            {
                // Enable calling on a number
                EnableWhatsAppCalling200Response result = apiInstance.EnableWhatsAppCalling(id, enableWhatsAppCallingRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.EnableWhatsAppCalling: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EnableWhatsAppCallingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Enable calling on a number
    ApiResponse<EnableWhatsAppCalling200Response> response = apiInstance.EnableWhatsAppCallingWithHttpInfo(id, enableWhatsAppCallingRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.EnableWhatsAppCallingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | WhatsAppPhoneNumber Mongo ID |  |
| **enableWhatsAppCallingRequest** | [**EnableWhatsAppCallingRequest**](EnableWhatsAppCallingRequest.md) |  |  |

### Return type

[**EnableWhatsAppCalling200Response**](EnableWhatsAppCalling200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calling enabled |  -  |
| **401** | Unauthorized |  -  |
| **404** | WhatsApp phone number not found |  -  |
| **422** | Not eligible to enable calling: not on usage-based billing, or the number&#39;s messaging limit is below Meta&#39;s ~2,000-daily-recipient threshold (TIER_250). Warm the number up to raise the limit. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwhatsappcall"></a>
# **GetWhatsAppCall**
> GetWhatsAppCall200Response GetWhatsAppCall (string callId, string accountId)

Get a single call

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
    public class GetWhatsAppCallExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var callId = "callId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get a single call
                GetWhatsAppCall200Response result = apiInstance.GetWhatsAppCall(callId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a single call
    ApiResponse<GetWhatsAppCall200Response> response = apiInstance.GetWhatsAppCallWithHttpInfo(callId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **callId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**GetWhatsAppCall200Response**](GetWhatsAppCall200Response.md)

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
| **404** | Call not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwhatsappcallestimate"></a>
# **GetWhatsAppCallEstimate**
> GetWhatsAppCallEstimate200Response GetWhatsAppCallEstimate (string accountId, string to, int? minutes = null, bool? recording = null)

Estimate per-minute cost for a destination

Returns a zero-markup estimated cost for an outbound call to the given destination, broken down by Meta + Telnyx + recording line items. Costs are pass-through, no margin applied. 

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
    public class GetWhatsAppCallEstimateExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var to = "to_example";  // string | 
            var minutes = 56;  // int? |  (optional) 
            var recording = true;  // bool? |  (optional) 

            try
            {
                // Estimate per-minute cost for a destination
                GetWhatsAppCallEstimate200Response result = apiInstance.GetWhatsAppCallEstimate(accountId, to, minutes, recording);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCallEstimate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppCallEstimateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Estimate per-minute cost for a destination
    ApiResponse<GetWhatsAppCallEstimate200Response> response = apiInstance.GetWhatsAppCallEstimateWithHttpInfo(accountId, to, minutes, recording);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCallEstimateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **to** | **string** |  |  |
| **minutes** | **int?** |  | [optional]  |
| **recording** | **bool?** |  | [optional]  |

### Return type

[**GetWhatsAppCallEstimate200Response**](GetWhatsAppCallEstimate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Estimate |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwhatsappcallpermissions"></a>
# **GetWhatsAppCallPermissions**
> GetWhatsAppCallPermissions200Response GetWhatsAppCallPermissions (string accountId, string to)

Check call permission for a consumer

Returns the permission state and the list of available actions for a given consumer wa_id (e.g. `start_call`, `send_call_permission_request`). Use this before placing a call to decide whether to prompt for consent first. 

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
    public class GetWhatsAppCallPermissionsExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var to = "to_example";  // string | Consumer wa_id (E.164, leading + optional)

            try
            {
                // Check call permission for a consumer
                GetWhatsAppCallPermissions200Response result = apiInstance.GetWhatsAppCallPermissions(accountId, to);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCallPermissions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppCallPermissionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check call permission for a consumer
    ApiResponse<GetWhatsAppCallPermissions200Response> response = apiInstance.GetWhatsAppCallPermissionsWithHttpInfo(accountId, to);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCallPermissionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **to** | **string** | Consumer wa_id (E.164, leading + optional) |  |

### Return type

[**GetWhatsAppCallPermissions200Response**](GetWhatsAppCallPermissions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Permission state |  -  |
| **401** | Unauthorized |  -  |
| **404** | WhatsApp account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwhatsappcallingconfig"></a>
# **GetWhatsAppCallingConfig**
> GetWhatsAppCallingConfig200Response GetWhatsAppCallingConfig (string accountId)

Get calling config for an account

Returns the local calling configuration snapshot for the connected WhatsApp account: whether calling is enabled, the forward-to destination URI, recording opt-in state, the WhatsAppPhoneNumber doc id (use as `{id}` on the calling-config write endpoints) and whether SIP digest credentials are stored (the encrypted password itself is never returned). 

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
    public class GetWhatsAppCallingConfigExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account ID

            try
            {
                // Get calling config for an account
                GetWhatsAppCallingConfig200Response result = apiInstance.GetWhatsAppCallingConfig(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCallingConfig: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppCallingConfigWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get calling config for an account
    ApiResponse<GetWhatsAppCallingConfig200Response> response = apiInstance.GetWhatsAppCallingConfigWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.GetWhatsAppCallingConfigWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account ID |  |

### Return type

[**GetWhatsAppCallingConfig200Response**](GetWhatsAppCallingConfig200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calling config |  -  |
| **401** | Unauthorized |  -  |
| **404** | WhatsApp phone number not found for this account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="initiatewhatsappcall"></a>
# **InitiateWhatsAppCall**
> InitiateWhatsAppCall200Response InitiateWhatsAppCall (InitiateWhatsAppCallRequest initiateWhatsAppCallRequest)

Initiate outbound call

Initiates an outbound Business-Initiated Call. The Telnyx-side SIP leg is originated server-side (Option B: SIP-first). Telnyx INVITEs Meta directly over TLS:5061 with the SIP digest credentials we captured at calling-enablement time). No client-side SDP is required; pass only `accountId` and `to`.  To send the consumer the call-consent prompt instead of placing a call, pass `action: \"send_call_permission_request\"` (+ optional `bodyText`). The consumer must tap Allow in WhatsApp before `start_call` is permitted; Meta limits the prompt to 1 per consumer per 24h (2 per 7 days) and requires an open 24h service window. 

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
    public class InitiateWhatsAppCallExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var initiateWhatsAppCallRequest = new InitiateWhatsAppCallRequest(); // InitiateWhatsAppCallRequest | 

            try
            {
                // Initiate outbound call
                InitiateWhatsAppCall200Response result = apiInstance.InitiateWhatsAppCall(initiateWhatsAppCallRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.InitiateWhatsAppCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the InitiateWhatsAppCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Initiate outbound call
    ApiResponse<InitiateWhatsAppCall200Response> response = apiInstance.InitiateWhatsAppCallWithHttpInfo(initiateWhatsAppCallRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.InitiateWhatsAppCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **initiateWhatsAppCallRequest** | [**InitiateWhatsAppCallRequest**](InitiateWhatsAppCallRequest.md) |  |  |

### Return type

[**InitiateWhatsAppCall200Response**](InitiateWhatsAppCall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Call originated; lifecycle continues asynchronously via webhooks. |  -  |
| **401** | Unauthorized |  -  |
| **409** | No active call permission — send a permission request first. |  -  |
| **422** | Calling not enabled, BIC country blocked, or missing Meta SIP credentials |  -  |
| **502** | Telnyx-side originate failed; the Call doc has been marked failed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listwhatsappcalls"></a>
# **ListWhatsAppCalls**
> ListWhatsAppCalls200Response ListWhatsAppCalls (string accountId, string? status = null, string? direction = null, DateTime? since = null, DateTime? until = null, int? limit = null)

List call history for an account

Compact history listing for a single connected account. Results are scoped to the resolved SocialAccount; profile-scoped team members cannot read calls on sibling accounts. 

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
    public class ListWhatsAppCallsExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var status = "ringing";  // string? |  (optional) 
            var direction = "inbound";  // string? |  (optional) 
            var since = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var until = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var limit = 56;  // int? |  (optional) 

            try
            {
                // List call history for an account
                ListWhatsAppCalls200Response result = apiInstance.ListWhatsAppCalls(accountId, status, direction, since, until, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.ListWhatsAppCalls: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWhatsAppCallsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List call history for an account
    ApiResponse<ListWhatsAppCalls200Response> response = apiInstance.ListWhatsAppCallsWithHttpInfo(accountId, status, direction, since, until, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.ListWhatsAppCallsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **status** | **string?** |  | [optional]  |
| **direction** | **string?** |  | [optional]  |
| **since** | **DateTime?** |  | [optional]  |
| **until** | **DateTime?** |  | [optional]  |
| **limit** | **int?** |  | [optional]  |

### Return type

[**ListWhatsAppCalls200Response**](ListWhatsAppCalls200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calls |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatewhatsappcalling"></a>
# **UpdateWhatsAppCalling**
> void UpdateWhatsAppCalling (string id, UpdateWhatsAppCallingRequest updateWhatsAppCallingRequest)

Update calling config

Update fields on an already-enabled number. Only fields present in the body are written; `undefined` leaves the stored value alone, explicit `null` clears a nullable field. No Meta side effect, this only changes local routing state consumed by the Telnyx webhook handler. 

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
    public class UpdateWhatsAppCallingExample
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
            var apiInstance = new WhatsAppCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var updateWhatsAppCallingRequest = new UpdateWhatsAppCallingRequest(); // UpdateWhatsAppCallingRequest | 

            try
            {
                // Update calling config
                apiInstance.UpdateWhatsAppCalling(id, updateWhatsAppCallingRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppCallingApi.UpdateWhatsAppCalling: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWhatsAppCallingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update calling config
    apiInstance.UpdateWhatsAppCallingWithHttpInfo(id, updateWhatsAppCallingRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppCallingApi.UpdateWhatsAppCallingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **updateWhatsAppCallingRequest** | [**UpdateWhatsAppCallingRequest**](UpdateWhatsAppCallingRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated |  -  |
| **401** | Unauthorized |  -  |
| **404** | WhatsApp phone number not found |  -  |
| **422** | Calling must be enabled before settings can be updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

