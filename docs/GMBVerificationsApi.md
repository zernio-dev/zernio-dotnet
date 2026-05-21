# Zernio.Api.GMBVerificationsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CompleteGoogleBusinessVerification**](GMBVerificationsApi.md#completegooglebusinessverification) | **POST** /v1/accounts/{accountId}/gmb-verifications/{verificationId}/complete | Complete a verification |
| [**FetchGoogleBusinessVerificationOptions**](GMBVerificationsApi.md#fetchgooglebusinessverificationoptions) | **POST** /v1/accounts/{accountId}/gmb-verifications/options | Fetch verification options |
| [**GetGoogleBusinessVerifications**](GMBVerificationsApi.md#getgooglebusinessverifications) | **GET** /v1/accounts/{accountId}/gmb-verifications | Get verification state |
| [**StartGoogleBusinessVerification**](GMBVerificationsApi.md#startgooglebusinessverification) | **POST** /v1/accounts/{accountId}/gmb-verifications | Start a verification |

<a id="completegooglebusinessverification"></a>
# **CompleteGoogleBusinessVerification**
> StartGoogleBusinessVerification200Response CompleteGoogleBusinessVerification (string accountId, string verificationId, CompleteGoogleBusinessVerificationRequest completeGoogleBusinessVerificationRequest, string? locationId = null)

Complete a verification

Completes a PENDING verification by submitting the PIN/code Google sent the business (postcard code, SMS PIN, etc.). On success the verification moves to COMPLETED.

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
    public class CompleteGoogleBusinessVerificationExample
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
            var apiInstance = new GMBVerificationsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Zernio account ID (from /v1/accounts)
            var verificationId = "verificationId_example";  // string | The last segment of a verification `name` from GET /gmb-verifications.
            var completeGoogleBusinessVerificationRequest = new CompleteGoogleBusinessVerificationRequest(); // CompleteGoogleBusinessVerificationRequest | 
            var locationId = "locationId_example";  // string? | Override which location to target. If omitted, uses the account's selected location. (optional) 

            try
            {
                // Complete a verification
                StartGoogleBusinessVerification200Response result = apiInstance.CompleteGoogleBusinessVerification(accountId, verificationId, completeGoogleBusinessVerificationRequest, locationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBVerificationsApi.CompleteGoogleBusinessVerification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CompleteGoogleBusinessVerificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Complete a verification
    ApiResponse<StartGoogleBusinessVerification200Response> response = apiInstance.CompleteGoogleBusinessVerificationWithHttpInfo(accountId, verificationId, completeGoogleBusinessVerificationRequest, locationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBVerificationsApi.CompleteGoogleBusinessVerificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Zernio account ID (from /v1/accounts) |  |
| **verificationId** | **string** | The last segment of a verification &#x60;name&#x60; from GET /gmb-verifications. |  |
| **completeGoogleBusinessVerificationRequest** | [**CompleteGoogleBusinessVerificationRequest**](CompleteGoogleBusinessVerificationRequest.md) |  |  |
| **locationId** | **string?** | Override which location to target. If omitted, uses the account&#39;s selected location. | [optional]  |

### Return type

[**StartGoogleBusinessVerification200Response**](StartGoogleBusinessVerification200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verification completed |  -  |
| **400** | Invalid request (e.g. wrong PIN or verification not pending) |  -  |
| **401** | Unauthorized or token invalid |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchgooglebusinessverificationoptions"></a>
# **FetchGoogleBusinessVerificationOptions**
> FetchGoogleBusinessVerificationOptions200Response FetchGoogleBusinessVerificationOptions (string accountId, FetchGoogleBusinessVerificationOptionsRequest fetchGoogleBusinessVerificationOptionsRequest, string? locationId = null)

Fetch verification options

Reports the verification methods Google currently offers for the location. Non-mutating (nothing is sent to the business). `languageCode` is required; service-area (\"CUSTOMER_LOCATION_ONLY\") businesses also require `context.address`, otherwise Google returns 400.

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
    public class FetchGoogleBusinessVerificationOptionsExample
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
            var apiInstance = new GMBVerificationsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Zernio account ID (from /v1/accounts)
            var fetchGoogleBusinessVerificationOptionsRequest = new FetchGoogleBusinessVerificationOptionsRequest(); // FetchGoogleBusinessVerificationOptionsRequest | 
            var locationId = "locationId_example";  // string? | Override which location to query. If omitted, uses the account's selected location. (optional) 

            try
            {
                // Fetch verification options
                FetchGoogleBusinessVerificationOptions200Response result = apiInstance.FetchGoogleBusinessVerificationOptions(accountId, fetchGoogleBusinessVerificationOptionsRequest, locationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBVerificationsApi.FetchGoogleBusinessVerificationOptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchGoogleBusinessVerificationOptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Fetch verification options
    ApiResponse<FetchGoogleBusinessVerificationOptions200Response> response = apiInstance.FetchGoogleBusinessVerificationOptionsWithHttpInfo(accountId, fetchGoogleBusinessVerificationOptionsRequest, locationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBVerificationsApi.FetchGoogleBusinessVerificationOptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Zernio account ID (from /v1/accounts) |  |
| **fetchGoogleBusinessVerificationOptionsRequest** | [**FetchGoogleBusinessVerificationOptionsRequest**](FetchGoogleBusinessVerificationOptionsRequest.md) |  |  |
| **locationId** | **string?** | Override which location to query. If omitted, uses the account&#39;s selected location. | [optional]  |

### Return type

[**FetchGoogleBusinessVerificationOptions200Response**](FetchGoogleBusinessVerificationOptions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verification options fetched |  -  |
| **400** | Invalid request (e.g. missing service business context, or missing languageCode) |  -  |
| **401** | Unauthorized or token invalid |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getgooglebusinessverifications"></a>
# **GetGoogleBusinessVerifications**
> GetGoogleBusinessVerifications200Response GetGoogleBusinessVerifications (string accountId, string? locationId = null)

Get verification state

Returns the location's Voice of Merchant state plus its verification history. `voiceOfMerchantState.hasVoiceOfMerchant` tells you whether the listing is verified and published; when it is false, `verify` reports whether a verification is already pending. Each entry in `verifications` has a `state` of PENDING, COMPLETED, or FAILED.

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
    public class GetGoogleBusinessVerificationsExample
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
            var apiInstance = new GMBVerificationsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Zernio account ID (from /v1/accounts)
            var locationId = "locationId_example";  // string? | Override which location to query. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. (optional) 

            try
            {
                // Get verification state
                GetGoogleBusinessVerifications200Response result = apiInstance.GetGoogleBusinessVerifications(accountId, locationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBVerificationsApi.GetGoogleBusinessVerifications: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGoogleBusinessVerificationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get verification state
    ApiResponse<GetGoogleBusinessVerifications200Response> response = apiInstance.GetGoogleBusinessVerificationsWithHttpInfo(accountId, locationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBVerificationsApi.GetGoogleBusinessVerificationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Zernio account ID (from /v1/accounts) |  |
| **locationId** | **string?** | Override which location to query. If omitted, uses the account&#39;s selected location. Use GET /gmb-locations to list valid IDs. | [optional]  |

### Return type

[**GetGoogleBusinessVerifications200Response**](GetGoogleBusinessVerifications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verification state fetched successfully |  -  |
| **400** | Not a Google Business account or missing location |  -  |
| **401** | Unauthorized or token invalid |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="startgooglebusinessverification"></a>
# **StartGoogleBusinessVerification**
> StartGoogleBusinessVerification200Response StartGoogleBusinessVerification (string accountId, StartGoogleBusinessVerificationRequest startGoogleBusinessVerificationRequest, string? locationId = null)

Start a verification

Starts a verification for the location. This is a mutating action: depending on `method`, Google mails a postcard, places a call, or sends an SMS/email to the business. Submit the resulting code with POST /gmb-verifications/{verificationId}/complete. Use POST /gmb-verifications/options first to discover which methods are eligible.

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
    public class StartGoogleBusinessVerificationExample
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
            var apiInstance = new GMBVerificationsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The Zernio account ID (from /v1/accounts)
            var startGoogleBusinessVerificationRequest = new StartGoogleBusinessVerificationRequest(); // StartGoogleBusinessVerificationRequest | 
            var locationId = "locationId_example";  // string? | Override which location to target. If omitted, uses the account's selected location. (optional) 

            try
            {
                // Start a verification
                StartGoogleBusinessVerification200Response result = apiInstance.StartGoogleBusinessVerification(accountId, startGoogleBusinessVerificationRequest, locationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBVerificationsApi.StartGoogleBusinessVerification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the StartGoogleBusinessVerificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Start a verification
    ApiResponse<StartGoogleBusinessVerification200Response> response = apiInstance.StartGoogleBusinessVerificationWithHttpInfo(accountId, startGoogleBusinessVerificationRequest, locationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBVerificationsApi.StartGoogleBusinessVerificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The Zernio account ID (from /v1/accounts) |  |
| **startGoogleBusinessVerificationRequest** | [**StartGoogleBusinessVerificationRequest**](StartGoogleBusinessVerificationRequest.md) |  |  |
| **locationId** | **string?** | Override which location to target. If omitted, uses the account&#39;s selected location. | [optional]  |

### Return type

[**StartGoogleBusinessVerification200Response**](StartGoogleBusinessVerification200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verification started |  -  |
| **400** | Invalid request (e.g. wrong field for the chosen method, or Google rejected it) |  -  |
| **401** | Unauthorized or token invalid |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

