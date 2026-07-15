# Zernio.Api.SMSApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AppealSmsRegistration**](SMSApi.md#appealsmsregistration) | **POST** /v1/sms/registrations/{id}/appeal | Appeal a rejected campaign |
| [**DisableSmsOnNumber**](SMSApi.md#disablesmsonnumber) | **DELETE** /v1/phone-numbers/{id}/sms | Disable SMS on a number |
| [**EnableSmsOnNumber**](SMSApi.md#enablesmsonnumber) | **POST** /v1/phone-numbers/{id}/sms | Enable SMS on a number |
| [**GetSmsRegistration**](SMSApi.md#getsmsregistration) | **GET** /v1/sms/registrations/{id} | Get a carrier registration |
| [**ListSmsOptOuts**](SMSApi.md#listsmsoptouts) | **GET** /v1/sms/opt-outs | List SMS opt-outs |
| [**ListSmsRegistrations**](SMSApi.md#listsmsregistrations) | **GET** /v1/sms/registrations | List carrier registrations |
| [**LookupSmsNumber**](SMSApi.md#lookupsmsnumber) | **GET** /v1/sms/lookup | Look up carrier + line type |
| [**ResendSmsRegistrationOtp**](SMSApi.md#resendsmsregistrationotp) | **POST** /v1/sms/registrations/{id}/resend-otp | Re-send the sole-prop OTP |
| [**ReuseSmsRegistrationForNumber**](SMSApi.md#reusesmsregistrationfornumber) | **POST** /v1/phone-numbers/{id}/sms/reuse-registration | Add number to SMS registration |
| [**SendSms**](SMSApi.md#sendsms) | **POST** /v1/sms/messages | Send an SMS/MMS |
| [**ShareSmsRegistration**](SMSApi.md#sharesmsregistration) | **POST** /v1/sms/registrations/share | Create a registration share link |
| [**StartSmsRegistration**](SMSApi.md#startsmsregistration) | **POST** /v1/sms/registrations | Start a carrier registration |
| [**UploadSmsOptInProof**](SMSApi.md#uploadsmsoptinproof) | **POST** /v1/sms/registrations/{id}/opt-in-proof | Upload opt-in form proof for an appeal |
| [**UploadSmsOptInProofFile**](SMSApi.md#uploadsmsoptinprooffile) | **POST** /v1/sms/opt-in-proof | Upload opt-in form proof |
| [**VerifySmsRegistrationOtp**](SMSApi.md#verifysmsregistrationotp) | **POST** /v1/sms/registrations/{id}/verify-otp | Submit the sole-prop OTP |

<a id="appealsmsregistration"></a>
# **AppealSmsRegistration**
> AppealSmsRegistration200Response AppealSmsRegistration (string id, AppealSmsRegistrationRequest appealSmsRegistrationRequest)

Appeal a rejected campaign

Appeals a rejected 10DLC campaign with the carrier registry. Only a registration that reached campaign creation can be appealed; a brand-level rejection should be fixed and re-verified instead. On success the registration returns to `pending`.  Content rejections (e.g. an opt-in flow without a verifiable form link, or unrealistic samples) should be FIXED in the same call: pass the corrected `messageFlow` / `sample1` / `sample2` and the campaign is updated before the appeal is filed, so the reviewer sees the new content. The current content is on `GET /v1/sms/registrations/{id}` (`campaignContent`). 

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
    public class AppealSmsRegistrationExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var appealSmsRegistrationRequest = new AppealSmsRegistrationRequest(); // AppealSmsRegistrationRequest | 

            try
            {
                // Appeal a rejected campaign
                AppealSmsRegistration200Response result = apiInstance.AppealSmsRegistration(id, appealSmsRegistrationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.AppealSmsRegistration: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppealSmsRegistrationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Appeal a rejected campaign
    ApiResponse<AppealSmsRegistration200Response> response = apiInstance.AppealSmsRegistrationWithHttpInfo(id, appealSmsRegistrationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.AppealSmsRegistrationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **appealSmsRegistrationRequest** | [**AppealSmsRegistrationRequest**](AppealSmsRegistrationRequest.md) |  |  |

### Return type

[**AppealSmsRegistration200Response**](AppealSmsRegistration200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Appeal submitted; the registration is pending again. |  -  |
| **400** | Registration has no campaign to appeal; fix the brand and re-verify instead |  -  |
| **401** | Unauthorized |  -  |
| **404** | Registration not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disablesmsonnumber"></a>
# **DisableSmsOnNumber**
> DisableSmsOnNumber200Response DisableSmsOnNumber (string id)

Disable SMS on a number

Turns off SMS for the number (deactivates its SMS account). The carrier registration is untouched, so re-enabling later just reactivates it, with no re-registration. 

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
    public class DisableSmsOnNumberExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Disable SMS on a number
                DisableSmsOnNumber200Response result = apiInstance.DisableSmsOnNumber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.DisableSmsOnNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisableSmsOnNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Disable SMS on a number
    ApiResponse<DisableSmsOnNumber200Response> response = apiInstance.DisableSmsOnNumberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.DisableSmsOnNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**DisableSmsOnNumber200Response**](DisableSmsOnNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | SMS disabled. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="enablesmsonnumber"></a>
# **EnableSmsOnNumber**
> EnableSmsOnNumber200Response EnableSmsOnNumber (string id)

Enable SMS on a number

Turns on SMS for one of your numbers. The number's real carrier capability is checked first: some number types can't do SMS at all (`smsCapable: false`), and a number still provisioning at the carrier returns `notReady: true` (try again once provisioning finishes).  US numbers additionally need a carrier registration before messages deliver; the response tells you which path applies: - `alreadyRegistered: true`: a prior registration still covers this   number; SMS was simply reactivated. - `reusable` set: you have an approved registration this number can   join in one click via   `POST /v1/phone-numbers/{id}/sms/reuse-registration`   (no new brand/campaign, no extra carrier fee). - `needsRegistration: true` and no `reusable`: start one via   `POST /v1/sms/registrations`.  Idempotent: re-running re-attempts any carrier-side setup that failed. 

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
    public class EnableSmsOnNumberExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | Phone number record ID (from GET /v1/phone-numbers).

            try
            {
                // Enable SMS on a number
                EnableSmsOnNumber200Response result = apiInstance.EnableSmsOnNumber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.EnableSmsOnNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EnableSmsOnNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Enable SMS on a number
    ApiResponse<EnableSmsOnNumber200Response> response = apiInstance.EnableSmsOnNumberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.EnableSmsOnNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Phone number record ID (from GET /v1/phone-numbers). |  |

### Return type

[**EnableSmsOnNumber200Response**](EnableSmsOnNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Result. Check &#x60;enabled&#x60;: a 200 with &#x60;enabled: false&#x60; means the number can&#39;t do SMS (&#x60;smsCapable: false&#x60;) or isn&#39;t ready yet (&#x60;notReady: true&#x60;). |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |
| **422** | This number is hosted by your own carrier (brought via WhatsApp embedded signup), so SMS can&#39;t be enabled on it. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getsmsregistration"></a>
# **GetSmsRegistration**
> GetSmsRegistration200Response GetSmsRegistration (string id)

Get a carrier registration

Poll this for approval progress after starting a registration.

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
    public class GetSmsRegistrationExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get a carrier registration
                GetSmsRegistration200Response result = apiInstance.GetSmsRegistration(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.GetSmsRegistration: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSmsRegistrationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a carrier registration
    ApiResponse<GetSmsRegistration200Response> response = apiInstance.GetSmsRegistrationWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.GetSmsRegistrationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**GetSmsRegistration200Response**](GetSmsRegistration200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Registration |  -  |
| **401** | Unauthorized |  -  |
| **404** | Registration not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listsmsoptouts"></a>
# **ListSmsOptOuts**
> ListSmsOptOuts200Response ListSmsOptOuts (string? format = null, int? limit = null)

List SMS opt-outs

The recipients who opted out of SMS (replied STOP) across your numbers, most recent first. Compliance surface: you must be able to see and export your opt-out list. Read-only: a recipient is re-subscribed only by replying START. Pass `format=csv` to download a CSV instead of JSON. 

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
    public class ListSmsOptOutsExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var format = "json";  // string? |  (optional)  (default to json)
            var limit = 500;  // int? |  (optional)  (default to 500)

            try
            {
                // List SMS opt-outs
                ListSmsOptOuts200Response result = apiInstance.ListSmsOptOuts(format, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.ListSmsOptOuts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSmsOptOutsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List SMS opt-outs
    ApiResponse<ListSmsOptOuts200Response> response = apiInstance.ListSmsOptOutsWithHttpInfo(format, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.ListSmsOptOutsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **format** | **string?** |  | [optional] [default to json] |
| **limit** | **int?** |  | [optional] [default to 500] |

### Return type

[**ListSmsOptOuts200Response**](ListSmsOptOuts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/csv


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Opt-out list |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listsmsregistrations"></a>
# **ListSmsRegistrations**
> ListSmsRegistrations200Response ListSmsRegistrations ()

List carrier registrations

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
    public class ListSmsRegistrationsExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);

            try
            {
                // List carrier registrations
                ListSmsRegistrations200Response result = apiInstance.ListSmsRegistrations();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.ListSmsRegistrations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSmsRegistrationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List carrier registrations
    ApiResponse<ListSmsRegistrations200Response> response = apiInstance.ListSmsRegistrationsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.ListSmsRegistrationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListSmsRegistrations200Response**](ListSmsRegistrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Registrations, newest first |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="lookupsmsnumber"></a>
# **LookupSmsNumber**
> LookupSmsNumber200Response LookupSmsNumber (string number)

Look up carrier + line type

Carrier name and line type (mobile / landline / voip / toll-free) for a number, plus `smsReachable` (landlines can't receive SMS). Use it to validate recipients before sending. Each lookup is billed by the carrier-data provider, so call it explicitly (e.g. pre-validating an opt-in list), not on every send. 

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
    public class LookupSmsNumberExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var number = "number_example";  // string | Number to look up (E.164; formatting is normalized).

            try
            {
                // Look up carrier + line type
                LookupSmsNumber200Response result = apiInstance.LookupSmsNumber(number);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.LookupSmsNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LookupSmsNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Look up carrier + line type
    ApiResponse<LookupSmsNumber200Response> response = apiInstance.LookupSmsNumberWithHttpInfo(number);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.LookupSmsNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **number** | **string** | Number to look up (E.164; formatting is normalized). |  |

### Return type

[**LookupSmsNumber200Response**](LookupSmsNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Lookup result. An unknown/invalid number returns lineType &#x60;unknown&#x60; with &#x60;smsReachable&#x60; false rather than an error. |  -  |
| **401** | Unauthorized |  -  |
| **502** | Lookup provider failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="resendsmsregistrationotp"></a>
# **ResendSmsRegistrationOtp**
> ResendSmsRegistrationOtp200Response ResendSmsRegistrationOtp (string id)

Re-send the sole-prop OTP

Re-sends the sole-proprietor verification PIN to the brand's mobile number — use it when the original code expired or never arrived. Only valid while the registration is pending and awaiting its OTP; rate limited to one send per minute. 

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
    public class ResendSmsRegistrationOtpExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Re-send the sole-prop OTP
                ResendSmsRegistrationOtp200Response result = apiInstance.ResendSmsRegistrationOtp(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.ResendSmsRegistrationOtp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResendSmsRegistrationOtpWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Re-send the sole-prop OTP
    ApiResponse<ResendSmsRegistrationOtp200Response> response = apiInstance.ResendSmsRegistrationOtpWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.ResendSmsRegistrationOtpWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ResendSmsRegistrationOtp200Response**](ResendSmsRegistrationOtp200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A new code was sent |  -  |
| **400** | The registration is not awaiting a verification code |  -  |
| **401** | Unauthorized |  -  |
| **404** | Registration not found |  -  |
| **429** | A code was just sent — wait a minute before requesting another |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reusesmsregistrationfornumber"></a>
# **ReuseSmsRegistrationForNumber**
> ReuseSmsRegistrationForNumber200Response ReuseSmsRegistrationForNumber (string id)

Add number to SMS registration

Attaches this number to your existing approved 10DLC campaign instead of running a fresh registration: the number inherits the campaign's approval (no new brand or campaign, no extra carrier fee). Enable SMS on the number first (`POST /v1/phone-numbers/{id}/sms`; its response tells you whether a reusable registration exists). 

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
    public class ReuseSmsRegistrationForNumberExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Add number to SMS registration
                ReuseSmsRegistrationForNumber200Response result = apiInstance.ReuseSmsRegistrationForNumber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.ReuseSmsRegistrationForNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReuseSmsRegistrationForNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add number to SMS registration
    ApiResponse<ReuseSmsRegistrationForNumber200Response> response = apiInstance.ReuseSmsRegistrationForNumberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.ReuseSmsRegistrationForNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ReuseSmsRegistrationForNumber200Response**](ReuseSmsRegistrationForNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Number added to the existing registration. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |
| **409** | No existing SMS registration to reuse for this number |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendsms"></a>
# **SendSms**
> SendSms200Response SendSms (SendSmsRequest sendSmsRequest, string? idempotencyKey = null)

Send an SMS/MMS

Sends an SMS (or MMS when `mediaUrls` is set) from one of your SMS-enabled numbers. At least one of `text` / `mediaUrls` is required. Both numbers are normalized to E.164, so `from` matches regardless of formatting and replies thread into the same inbox conversation.  US numbers must have an approved carrier registration (`/v1/sms/registrations`) before messages deliver.  **Idempotency:** send an `Idempotency-Key` header to make retries safe: same key + same body replays the original response instead of sending a second message; same key + different body returns 422; a key still in flight returns 409. 

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
    public class SendSmsExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var sendSmsRequest = new SendSmsRequest(); // SendSmsRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes send retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Send an SMS/MMS
                SendSms200Response result = apiInstance.SendSms(sendSmsRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.SendSms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendSmsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send an SMS/MMS
    ApiResponse<SendSms200Response> response = apiInstance.SendSmsWithHttpInfo(sendSmsRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.SendSmsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendSmsRequest** | [**SendSmsRequest**](SendSmsRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes send retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**SendSms200Response**](SendSms200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Message accepted for delivery. |  -  |
| **401** | Unauthorized |  -  |
| **404** | No SMS-enabled number matches &#x60;from&#x60; |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | Idempotency-Key reused with a different body |  -  |
| **502** | Carrier-side send failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sharesmsregistration"></a>
# **ShareSmsRegistration**
> ShareSmsRegistration200Response ShareSmsRegistration (ShareSmsRegistrationRequest shareSmsRegistrationRequest)

Create a registration share link

Creates a single-use, expiring link (valid 7 days) that lets someone else (whoever has the legal business details) fill in the carrier registration form for one of your numbers, without a Zernio login. The registration is created under your account once the form is submitted. 

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
    public class ShareSmsRegistrationExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var shareSmsRegistrationRequest = new ShareSmsRegistrationRequest(); // ShareSmsRegistrationRequest | 

            try
            {
                // Create a registration share link
                ShareSmsRegistration200Response result = apiInstance.ShareSmsRegistration(shareSmsRegistrationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.ShareSmsRegistration: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ShareSmsRegistrationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a registration share link
    ApiResponse<ShareSmsRegistration200Response> response = apiInstance.ShareSmsRegistrationWithHttpInfo(shareSmsRegistrationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.ShareSmsRegistrationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shareSmsRegistrationRequest** | [**ShareSmsRegistrationRequest**](ShareSmsRegistrationRequest.md) |  |  |

### Return type

[**ShareSmsRegistration200Response**](ShareSmsRegistration200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Share link created. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="startsmsregistration"></a>
# **StartSmsRegistration**
> StartSmsRegistration200Response StartSmsRegistration (StartSmsRegistrationRequest startSmsRegistrationRequest)

Start a carrier registration

Starts the US carrier registration that a number needs before SMS delivers: 10DLC (standard company or sole-proprietor) or toll-free verification. 10DLC needs `brand` + `campaign`; toll-free needs `tollFree`. Approval is asynchronous; poll `GET /v1/sms/registrations/{id}` (sole-prop registrations first need the OTP step: a code is texted to the brand's mobile number, submit it via `/verify-otp`).  Already have an approved registration? Add another number to it with `POST /v1/phone-numbers/{id}/sms/reuse-registration` instead of registering (and paying the carrier brand fee) again.  Rather have your client fill in the legal business details? Create a share link with `POST /v1/sms/registrations/share`. 

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
    public class StartSmsRegistrationExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var startSmsRegistrationRequest = new StartSmsRegistrationRequest(); // StartSmsRegistrationRequest | 

            try
            {
                // Start a carrier registration
                StartSmsRegistration200Response result = apiInstance.StartSmsRegistration(startSmsRegistrationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.StartSmsRegistration: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the StartSmsRegistrationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start a carrier registration
    ApiResponse<StartSmsRegistration200Response> response = apiInstance.StartSmsRegistrationWithHttpInfo(startSmsRegistrationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.StartSmsRegistrationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startSmsRegistrationRequest** | [**StartSmsRegistrationRequest**](StartSmsRegistrationRequest.md) |  |  |

### Return type

[**StartSmsRegistration200Response**](StartSmsRegistration200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Registration submitted. |  -  |
| **401** | Unauthorized |  -  |
| **422** | Carrier registry rejected a field; &#x60;param&#x60; names it when known. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadsmsoptinproof"></a>
# **UploadSmsOptInProof**
> UploadSmsOptInProofFile200Response UploadSmsOptInProof (string id, FileParameter file)

Upload opt-in form proof for an appeal

Hosts a screenshot (or PDF) of your SMS opt-in form and returns its public URL. Carrier reviewers reject campaigns whose consent can't be verified and ask for a \"link/screenshot of the opt-in form\" — the registry has no attachment field, so include the returned URL inside the `messageFlow` you submit with the appeal (`POST /v1/sms/registrations/{id}/appeal`). 

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
    public class UploadSmsOptInProofExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter | PNG, JPG, WebP, GIF or PDF, max 4MB.

            try
            {
                // Upload opt-in form proof for an appeal
                UploadSmsOptInProofFile200Response result = apiInstance.UploadSmsOptInProof(id, file);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.UploadSmsOptInProof: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadSmsOptInProofWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload opt-in form proof for an appeal
    ApiResponse<UploadSmsOptInProofFile200Response> response = apiInstance.UploadSmsOptInProofWithHttpInfo(id, file);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.UploadSmsOptInProofWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **file** | **FileParameter****FileParameter** | PNG, JPG, WebP, GIF or PDF, max 4MB. |  |

### Return type

[**UploadSmsOptInProofFile200Response**](UploadSmsOptInProofFile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File hosted. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Registration not found |  -  |
| **422** | Unsupported file type or file too large |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadsmsoptinprooffile"></a>
# **UploadSmsOptInProofFile**
> UploadSmsOptInProofFile200Response UploadSmsOptInProofFile (FileParameter file)

Upload opt-in form proof

Hosts a screenshot (or PDF) of your SMS opt-in form and returns its public URL. Include that URL in the campaign's `messageFlow` (the opt-in workflow text) — the carrier registry has no attachment field, so reviewers verify consent by opening links in that answer. Works before a registration exists (use it when registering) and for appeals. `/v1/sms/registrations/{id}/opt-in-proof` is an alias. 

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
    public class UploadSmsOptInProofFileExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter | PNG, JPG, WebP, GIF or PDF, max 4MB.

            try
            {
                // Upload opt-in form proof
                UploadSmsOptInProofFile200Response result = apiInstance.UploadSmsOptInProofFile(file);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.UploadSmsOptInProofFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadSmsOptInProofFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload opt-in form proof
    ApiResponse<UploadSmsOptInProofFile200Response> response = apiInstance.UploadSmsOptInProofFileWithHttpInfo(file);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.UploadSmsOptInProofFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **file** | **FileParameter****FileParameter** | PNG, JPG, WebP, GIF or PDF, max 4MB. |  |

### Return type

[**UploadSmsOptInProofFile200Response**](UploadSmsOptInProofFile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File hosted. |  -  |
| **401** | Unauthorized |  -  |
| **422** | Unsupported file type or file too large |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="verifysmsregistrationotp"></a>
# **VerifySmsRegistrationOtp**
> VerifySmsRegistrationOtp200Response VerifySmsRegistrationOtp (string id, VerifySmsRegistrationOtpRequest verifySmsRegistrationOtpRequest)

Submit the sole-prop OTP

Completes sole-proprietor 10DLC brand verification by submitting the one-time PIN texted to the brand's mobile number. On success the registration continues to campaign creation automatically. 

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
    public class VerifySmsRegistrationOtpExample
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
            var apiInstance = new SMSApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var verifySmsRegistrationOtpRequest = new VerifySmsRegistrationOtpRequest(); // VerifySmsRegistrationOtpRequest | 

            try
            {
                // Submit the sole-prop OTP
                VerifySmsRegistrationOtp200Response result = apiInstance.VerifySmsRegistrationOtp(id, verifySmsRegistrationOtpRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSApi.VerifySmsRegistrationOtp: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VerifySmsRegistrationOtpWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit the sole-prop OTP
    ApiResponse<VerifySmsRegistrationOtp200Response> response = apiInstance.VerifySmsRegistrationOtpWithHttpInfo(id, verifySmsRegistrationOtpRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSApi.VerifySmsRegistrationOtpWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **verifySmsRegistrationOtpRequest** | [**VerifySmsRegistrationOtpRequest**](VerifySmsRegistrationOtpRequest.md) |  |  |

### Return type

[**VerifySmsRegistrationOtp200Response**](VerifySmsRegistrationOtp200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OTP result |  -  |
| **401** | Unauthorized |  -  |
| **404** | Registration not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

