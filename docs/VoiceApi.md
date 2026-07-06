# Zernio.Api.VoiceApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateVoiceCall**](VoiceApi.md#createvoicecall) | **POST** /v1/voice/calls | Place an outbound phone call |
| [**CreateVoiceWebSession**](VoiceApi.md#createvoicewebsession) | **POST** /v1/voice/calls/web | Mint a browser softphone session |
| [**DialVoiceWebCall**](VoiceApi.md#dialvoicewebcall) | **POST** /v1/voice/calls/web/dial | Dial from the browser softphone |
| [**DisableVoiceOnNumber**](VoiceApi.md#disablevoiceonnumber) | **DELETE** /v1/phone-numbers/{id}/voice | Disable phone calling on a number |
| [**EnableVoiceOnNumber**](VoiceApi.md#enablevoiceonnumber) | **POST** /v1/phone-numbers/{id}/voice | Enable phone calling on a number |
| [**EndVoiceCall**](VoiceApi.md#endvoicecall) | **POST** /v1/voice/calls/{id}/end | Hang up a live call |
| [**GetVoiceCall**](VoiceApi.md#getvoicecall) | **GET** /v1/voice/calls/{id} | Get a phone call |
| [**GetVoiceCallEstimate**](VoiceApi.md#getvoicecallestimate) | **GET** /v1/voice/calls/estimate | Estimate call cost |
| [**GetVoiceCallRecording**](VoiceApi.md#getvoicecallrecording) | **GET** /v1/voice/calls/{id}/recording | Get a call recording |
| [**ListVoiceCalls**](VoiceApi.md#listvoicecalls) | **GET** /v1/voice/calls | List phone calls |
| [**TransferVoiceCall**](VoiceApi.md#transfervoicecall) | **POST** /v1/voice/calls/{id}/transfer | Blind-transfer a live call |

<a id="createvoicecall"></a>
# **CreateVoiceCall**
> CreateVoiceCall200Response CreateVoiceCall (CreateVoiceCallRequest createVoiceCallRequest, string? idempotencyKey = null)

Place an outbound phone call

Dials `to` FROM one of your voice-enabled numbers and, on answer, bridges the callee to the number's stored forward destination, or to the per-call `forwardTo` override. Destinations can be your own AI voice agent (Vapi/Retell), a phone, or a SIP endpoint. An optional `greeting` is spoken to the callee before the bridge.  The 200 response means the call is dialing; the lifecycle continues asynchronously (track it via `GET /v1/voice/calls/{id}` or the `call.*` webhooks). Outbound calls are capped per rolling hour (429 when hit).  **Idempotency:** send an `Idempotency-Key` header to make retries safe; same key + same body replays the original response instead of dialing (and billing) a second call. 

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
    public class CreateVoiceCallExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var createVoiceCallRequest = new CreateVoiceCallRequest(); // CreateVoiceCallRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes dial retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Place an outbound phone call
                CreateVoiceCall200Response result = apiInstance.CreateVoiceCall(createVoiceCallRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.CreateVoiceCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateVoiceCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Place an outbound phone call
    ApiResponse<CreateVoiceCall200Response> response = apiInstance.CreateVoiceCallWithHttpInfo(createVoiceCallRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.CreateVoiceCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createVoiceCallRequest** | [**CreateVoiceCallRequest**](CreateVoiceCallRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes dial retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**CreateVoiceCall200Response**](CreateVoiceCall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Call originated; lifecycle continues asynchronously. |  -  |
| **401** | Unauthorized |  -  |
| **422** | No voice-enabled number matches &#x60;fromNumber&#x60;, or no forward destination configured (set the number&#39;s forward or pass &#x60;forwardTo&#x60;). |  -  |
| **429** | Outbound call limit reached (per rolling hour). |  -  |
| **502** | Carrier-side originate failed; the call has been marked failed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createvoicewebsession"></a>
# **CreateVoiceWebSession**
> CreateVoiceWebSession200Response CreateVoiceWebSession ()

Mint a browser softphone session

Step 1 of the two-step browser softphone handshake. Mints a WebRTC session (token + credential) the browser registers with the `@telnyx/webrtc` SDK. Once registered, call `POST /v1/voice/calls/web/dial` with the returned `credentialId` to place the call. The split avoids bridging to a browser that has not finished registering. The token lives ~1 hour (it must outlive the whole call, not just the handshake). 

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
    public class CreateVoiceWebSessionExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);

            try
            {
                // Mint a browser softphone session
                CreateVoiceWebSession200Response result = apiInstance.CreateVoiceWebSession();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.CreateVoiceWebSession: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateVoiceWebSessionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mint a browser softphone session
    ApiResponse<CreateVoiceWebSession200Response> response = apiInstance.CreateVoiceWebSessionWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.CreateVoiceWebSessionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**CreateVoiceWebSession200Response**](CreateVoiceWebSession200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | WebRTC session minted. |  -  |
| **401** | Unauthorized |  -  |
| **502** | Failed to mint the WebRTC session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="dialvoicewebcall"></a>
# **DialVoiceWebCall**
> DialVoiceWebCall200Response DialVoiceWebCall (DialVoiceWebCallRequest dialVoiceWebCallRequest)

Dial from the browser softphone

Step 2 of the browser softphone handshake: places an outbound call whose answered leg is bridged to the browser registered with the credential from `POST /v1/voice/calls/web`. The call runs through the normal outbound lane, so it is logged as outbound (from = your number, to = target) and recorded per the number's settings. 

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
    public class DialVoiceWebCallExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var dialVoiceWebCallRequest = new DialVoiceWebCallRequest(); // DialVoiceWebCallRequest | 

            try
            {
                // Dial from the browser softphone
                DialVoiceWebCall200Response result = apiInstance.DialVoiceWebCall(dialVoiceWebCallRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.DialVoiceWebCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DialVoiceWebCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Dial from the browser softphone
    ApiResponse<DialVoiceWebCall200Response> response = apiInstance.DialVoiceWebCallWithHttpInfo(dialVoiceWebCallRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.DialVoiceWebCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dialVoiceWebCallRequest** | [**DialVoiceWebCallRequest**](DialVoiceWebCallRequest.md) |  |  |

### Return type

[**DialVoiceWebCall200Response**](DialVoiceWebCall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Call originated; answer/bridge continue asynchronously. |  -  |
| **401** | Unauthorized |  -  |
| **422** | Invalid or unknown WebRTC credential, or no voice-enabled number matches &#x60;fromNumber&#x60; |  -  |
| **429** | Outbound call limit reached (per rolling hour). |  -  |
| **502** | Carrier-side originate failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disablevoiceonnumber"></a>
# **DisableVoiceOnNumber**
> DisableVoiceOnNumber200Response DisableVoiceOnNumber (string id)

Disable phone calling on a number

Turns off PSTN calling for the number. The stored forward destination and settings are preserved, so re-enabling restores the prior config. 

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
    public class DisableVoiceOnNumberExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Disable phone calling on a number
                DisableVoiceOnNumber200Response result = apiInstance.DisableVoiceOnNumber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.DisableVoiceOnNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisableVoiceOnNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Disable phone calling on a number
    ApiResponse<DisableVoiceOnNumber200Response> response = apiInstance.DisableVoiceOnNumberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.DisableVoiceOnNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**DisableVoiceOnNumber200Response**](DisableVoiceOnNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Voice disabled. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="enablevoiceonnumber"></a>
# **EnableVoiceOnNumber**
> EnableVoiceOnNumber200Response EnableVoiceOnNumber (string id, EnableVoiceOnNumberRequest? enableVoiceOnNumberRequest = null)

Enable phone calling on a number

Turns on regular phone (PSTN) calling for one of your numbers and configures how inbound calls are handled. Inbound calls route to `forwardTo`: your own AI voice agent (Vapi/Retell), a phone, or a SIP endpoint. Optional extras: voicemail, business-hours windows, an IVR menu, a caller blocklist, recording, and transcription. A number can also be voice-enabled with no forward (outbound-only).  Idempotent, and doubles as the settings update: only fields present in the body are written. Omitting `forwardTo` preserves the current destination; sending an empty string clears it. 

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
    public class EnableVoiceOnNumberExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | Phone number record ID (from GET /v1/phone-numbers).
            var enableVoiceOnNumberRequest = new EnableVoiceOnNumberRequest?(); // EnableVoiceOnNumberRequest? |  (optional) 

            try
            {
                // Enable phone calling on a number
                EnableVoiceOnNumber200Response result = apiInstance.EnableVoiceOnNumber(id, enableVoiceOnNumberRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.EnableVoiceOnNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EnableVoiceOnNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Enable phone calling on a number
    ApiResponse<EnableVoiceOnNumber200Response> response = apiInstance.EnableVoiceOnNumberWithHttpInfo(id, enableVoiceOnNumberRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.EnableVoiceOnNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Phone number record ID (from GET /v1/phone-numbers). |  |
| **enableVoiceOnNumberRequest** | [**EnableVoiceOnNumberRequest?**](EnableVoiceOnNumberRequest?.md) |  | [optional]  |

### Return type

[**EnableVoiceOnNumber200Response**](EnableVoiceOnNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Voice enabled; the full effective voice config is echoed back. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |
| **422** | This number is hosted by your own carrier (brought via WhatsApp embedded signup), so calls can&#39;t be enabled on it. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="endvoicecall"></a>
# **EndVoiceCall**
> EndVoiceCall200Response EndVoiceCall (string id)

Hang up a live call

Hangs up a live call on demand. Idempotent: ending a call that already ended (or never connected) returns success with the call's current status. Final duration/cost are written asynchronously when the hangup event lands, so the call doc may briefly still show its prior status. 

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
    public class EndVoiceCallExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Hang up a live call
                EndVoiceCall200Response result = apiInstance.EndVoiceCall(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.EndVoiceCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EndVoiceCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Hang up a live call
    ApiResponse<EndVoiceCall200Response> response = apiInstance.EndVoiceCallWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.EndVoiceCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**EndVoiceCall200Response**](EndVoiceCall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hangup issued (or the call was already over). |  -  |
| **401** | Unauthorized |  -  |
| **404** | Call not found |  -  |
| **502** | Carrier-side hangup failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getvoicecall"></a>
# **GetVoiceCall**
> GetVoiceCall200Response GetVoiceCall (string id)

Get a phone call

Full call detail, including the transcript segments when transcription was on.

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
    public class GetVoiceCallExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get a phone call
                GetVoiceCall200Response result = apiInstance.GetVoiceCall(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.GetVoiceCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetVoiceCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a phone call
    ApiResponse<GetVoiceCall200Response> response = apiInstance.GetVoiceCallWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.GetVoiceCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**GetVoiceCall200Response**](GetVoiceCall200Response.md)

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

<a id="getvoicecallestimate"></a>
# **GetVoiceCallEstimate**
> GetVoiceCallEstimate200Response GetVoiceCallEstimate (string to, int? minutes = null, bool? recording = null, bool? transcription = null)

Estimate call cost

Pre-call cost estimate for a PSTN call: the carrier leg plus optional recording and transcription add-ons. Same billing formula as the post-call invoice, so the quote and the final charge can't disagree. The per-minute figure is deliberately conservative (the real cost comes from the settled carrier record after the call), so estimates trend slightly over the actual invoice. Parity endpoint of `GET /v1/whatsapp/calls/estimate`, minus the Meta line (PSTN calls have no separate Meta bill, so `totalCostUSD` equals `billableCostUSD`). 

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
    public class GetVoiceCallEstimateExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var to = "to_example";  // string | Destination number, E.164 (leading + optional).
            var minutes = 1;  // int? |  (optional)  (default to 1)
            var recording = true;  // bool? |  (optional) 
            var transcription = true;  // bool? |  (optional) 

            try
            {
                // Estimate call cost
                GetVoiceCallEstimate200Response result = apiInstance.GetVoiceCallEstimate(to, minutes, recording, transcription);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.GetVoiceCallEstimate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetVoiceCallEstimateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Estimate call cost
    ApiResponse<GetVoiceCallEstimate200Response> response = apiInstance.GetVoiceCallEstimateWithHttpInfo(to, minutes, recording, transcription);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.GetVoiceCallEstimateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **to** | **string** | Destination number, E.164 (leading + optional). |  |
| **minutes** | **int?** |  | [optional] [default to 1] |
| **recording** | **bool?** |  | [optional]  |
| **transcription** | **bool?** |  | [optional]  |

### Return type

[**GetVoiceCallEstimate200Response**](GetVoiceCallEstimate200Response.md)

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

<a id="getvoicecallrecording"></a>
# **GetVoiceCallRecording**
> GetWhatsAppCallRecording200Response GetVoiceCallRecording (string id, string? varAs = null)

Get a call recording

Resolves a fresh, playable MP3 URL for the call's recording (provider-signed URLs expire ~10 minutes after signing, so this endpoint re-signs on demand). Default responds `302 Found` redirecting to the fresh URL; pass `as=json` to receive `{ url }` instead. 

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
    public class GetVoiceCallRecordingExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var varAs = "json";  // string? | `json` returns `{ url }` instead of a 302 redirect. (optional) 

            try
            {
                // Get a call recording
                GetWhatsAppCallRecording200Response result = apiInstance.GetVoiceCallRecording(id, varAs);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.GetVoiceCallRecording: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetVoiceCallRecordingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a call recording
    ApiResponse<GetWhatsAppCallRecording200Response> response = apiInstance.GetVoiceCallRecordingWithHttpInfo(id, varAs);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.GetVoiceCallRecordingWithHttpInfo: " + e.Message);
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
| **404** | Call not found, or no recording is available for this call |  -  |
| **502** | Recording provider lookup failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listvoicecalls"></a>
# **ListVoiceCalls**
> ListVoiceCalls200Response ListVoiceCalls (string? status = null, string? direction = null, string? number = null, DateTime? before = null, int? limit = null)

List phone calls

Your PSTN voice calls (inbound + outbound), newest first. Cursor pagination: pass the returned `nextCursor` as `before` for the next page. For a history that also includes WhatsApp calls, use `GET /v1/calls`. 

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
    public class ListVoiceCallsExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var status = "ringing";  // string? |  (optional) 
            var direction = "inbound";  // string? |  (optional) 
            var number = "number_example";  // string? | Exact filter: calls involving this number (typically one of your DIDs). E.164, leading + optional. (optional) 
            var before = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // List phone calls
                ListVoiceCalls200Response result = apiInstance.ListVoiceCalls(status, direction, number, before, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.ListVoiceCalls: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListVoiceCallsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List phone calls
    ApiResponse<ListVoiceCalls200Response> response = apiInstance.ListVoiceCallsWithHttpInfo(status, direction, number, before, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.ListVoiceCallsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string?** |  | [optional]  |
| **direction** | **string?** |  | [optional]  |
| **number** | **string?** | Exact filter: calls involving this number (typically one of your DIDs). E.164, leading + optional. | [optional]  |
| **before** | **DateTime?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |

### Return type

[**ListVoiceCalls200Response**](ListVoiceCalls200Response.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="transfervoicecall"></a>
# **TransferVoiceCall**
> TransferVoiceCall200Response TransferVoiceCall (string id, TransferVoiceCallRequest transferVoiceCallRequest)

Blind-transfer a live call

Moves the call's current leg to a new destination (a phone number or a SIP endpoint). This is a BLIND transfer: control of the leg is handed off and the call ends normally when the transferred leg hangs up. The caller ID presented on the transfer leg is always your own number. 

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
    public class TransferVoiceCallExample
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
            var apiInstance = new VoiceApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var transferVoiceCallRequest = new TransferVoiceCallRequest(); // TransferVoiceCallRequest | 

            try
            {
                // Blind-transfer a live call
                TransferVoiceCall200Response result = apiInstance.TransferVoiceCall(id, transferVoiceCallRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VoiceApi.TransferVoiceCall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TransferVoiceCallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Blind-transfer a live call
    ApiResponse<TransferVoiceCall200Response> response = apiInstance.TransferVoiceCallWithHttpInfo(id, transferVoiceCallRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VoiceApi.TransferVoiceCallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **transferVoiceCallRequest** | [**TransferVoiceCallRequest**](TransferVoiceCallRequest.md) |  |  |

### Return type

[**TransferVoiceCall200Response**](TransferVoiceCall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Transfer issued. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Call not found |  -  |
| **409** | Call is not connected yet, or has already ended |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

