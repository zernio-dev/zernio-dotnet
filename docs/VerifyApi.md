# Zernio.Api.VerifyApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CheckVerification**](VerifyApi.md#checkverification) | **POST** /v1/verify/verifications/{verificationId}/check | Check a verification code |
| [**CreateVerification**](VerifyApi.md#createverification) | **POST** /v1/verify/verifications | Send a verification code |
| [**GetVerification**](VerifyApi.md#getverification) | **GET** /v1/verify/verifications/{verificationId} | Get a verification |

<a id="checkverification"></a>
# **CheckVerification**
> CheckVerification200Response CheckVerification (string verificationId, CheckVerificationRequest checkVerificationRequest)

Check a verification code

Verify the code the user typed. Wrong, expired, and exhausted codes answer 200 with `valid: false` and the settled `status`. Only an unknown id is a 404. A correct code consumes the verification (single-use, `status: approved`) and fires the `verification.approved` webhook; the 5th wrong attempt settles it as `max_attempts_reached` and fires `verification.failed`. 

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
    public class CheckVerificationExample
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
            var apiInstance = new VerifyApi(httpClient, config, httpClientHandler);
            var verificationId = "verificationId_example";  // string | 
            var checkVerificationRequest = new CheckVerificationRequest(); // CheckVerificationRequest | 

            try
            {
                // Check a verification code
                CheckVerification200Response result = apiInstance.CheckVerification(verificationId, checkVerificationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VerifyApi.CheckVerification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckVerificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check a verification code
    ApiResponse<CheckVerification200Response> response = apiInstance.CheckVerificationWithHttpInfo(verificationId, checkVerificationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VerifyApi.CheckVerificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **verificationId** | **string** |  |  |
| **checkVerificationRequest** | [**CheckVerificationRequest**](CheckVerificationRequest.md) |  |  |

### Return type

[**CheckVerification200Response**](CheckVerification200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Check result: the verification plus &#x60;valid&#x60;. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Verification not found (or already reaped). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createverification"></a>
# **CreateVerification**
> Verification CreateVerification (CreateVerificationRequest createVerificationRequest)

Send a verification code

Generate a one-time code, deliver it to the recipient, and store only its hash. Check the user-typed code with POST /v1/verify/verifications/{verificationId}/check.  Re-POSTing for the same (channel, to) while a verification is active RESENDS a fresh code on the existing verification (200 with `resend: true`) instead of creating a new one; resends are limited to one per 60 seconds (429 with `retryAfterSeconds` inside the cooldown). The stored brandName/codeLength/ttlMinutes win on a resend.  Codes deliver from a number on your account (`from` optional when you own exactly one number on the channel), always with a fixed template:  - `sms`: from an SMS-enabled number. Each accepted send bills one   verification fee plus the standard message rate. - `whatsapp`: from a connected WhatsApp number, as a Meta   AUTHENTICATION template with a copy-code button. The first   WhatsApp verification on a WhatsApp Business Account creates the   `zernio_verify_code` template there and answers 422   `template_pending` until Meta approves it (usually minutes; retry   after `retryAfterSeconds`). Meta fixes the message text, so   `brandName` is not shown and the code's validity is not stated in   the message (`ttlMinutes` is still enforced). Each accepted send   bills one verification fee; Meta bills its authentication rate to   your WhatsApp Business Account. 

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
    public class CreateVerificationExample
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
            var apiInstance = new VerifyApi(httpClient, config, httpClientHandler);
            var createVerificationRequest = new CreateVerificationRequest(); // CreateVerificationRequest | 

            try
            {
                // Send a verification code
                Verification result = apiInstance.CreateVerification(createVerificationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VerifyApi.CreateVerification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateVerificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send a verification code
    ApiResponse<Verification> response = apiInstance.CreateVerificationWithHttpInfo(createVerificationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VerifyApi.CreateVerificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createVerificationRequest** | [**CreateVerificationRequest**](CreateVerificationRequest.md) |  |  |

### Return type

[**Verification**](Verification.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Active verification found: a fresh code was resent (&#x60;resend: true&#x60;). |  -  |
| **201** | Verification created and the code sent. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Verifications require usage-based billing. |  -  |
| **404** | The &#39;from&#39; number is not an SMS-enabled (sms) or connected WhatsApp (whatsapp) number on this account. |  -  |
| **409** | The recipient has opted out of messages from your number. |  -  |
| **422** | No number on your account for the channel (code linked_account_required), or, on whatsapp, the verification template is still in Meta review (code template_pending, retry after &#x60;retryAfterSeconds&#x60;) or was rejected, paused or disabled by Meta (code template_rejected, &#x60;details.status&#x60; and &#x60;details.reason&#x60; say why), or the WhatsApp number needs reconnection (code invalid_resource_state). |  -  |
| **429** | Resend cooldown or a send cap was hit; &#x60;retryAfterSeconds&#x60; says when to retry. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getverification"></a>
# **GetVerification**
> Verification GetVerification (string verificationId)

Get a verification

Current state of a verification. `status` is effective (a pending code past its expiry reads as `expired`). Verification records are deleted 24 hours after creation, after which this returns 404. 

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
    public class GetVerificationExample
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
            var apiInstance = new VerifyApi(httpClient, config, httpClientHandler);
            var verificationId = "verificationId_example";  // string | 

            try
            {
                // Get a verification
                Verification result = apiInstance.GetVerification(verificationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VerifyApi.GetVerification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetVerificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a verification
    ApiResponse<Verification> response = apiInstance.GetVerificationWithHttpInfo(verificationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VerifyApi.GetVerificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **verificationId** | **string** |  |  |

### Return type

[**Verification**](Verification.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The verification. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Verification not found (or already reaped). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

