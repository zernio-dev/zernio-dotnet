# Zernio.Api.BrandedCallingApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AttachBrandedCallingNumbers**](BrandedCallingApi.md#attachbrandedcallingnumbers) | **POST** /v1/branded-calling/identities/{id}/numbers | Attach numbers to a verified identity |
| [**ConfirmBrandedCallingAuthorizerEmail**](BrandedCallingApi.md#confirmbrandedcallingauthorizeremail) | **POST** /v1/branded-calling/identities/{id}/verify-email/confirm | Confirm the authorizer&#39;s code |
| [**CreateBrandedCallingEnterprise**](BrandedCallingApi.md#createbrandedcallingenterprise) | **POST** /v1/branded-calling/enterprises | Register a business for Branded Calling |
| [**CreateBrandedCallingIdentity**](BrandedCallingApi.md#createbrandedcallingidentity) | **POST** /v1/branded-calling/identities | Create a caller identity |
| [**DeleteBrandedCallingEnterprise**](BrandedCallingApi.md#deletebrandedcallingenterprise) | **DELETE** /v1/branded-calling/enterprises/{id} | Delete a registered business |
| [**DeleteBrandedCallingIdentity**](BrandedCallingApi.md#deletebrandedcallingidentity) | **DELETE** /v1/branded-calling/identities/{id} | Delete a caller identity |
| [**DetachBrandedCallingNumbers**](BrandedCallingApi.md#detachbrandedcallingnumbers) | **DELETE** /v1/branded-calling/identities/{id}/numbers | Detach numbers from an identity |
| [**GetBrandedCallingEnterprise**](BrandedCallingApi.md#getbrandedcallingenterprise) | **GET** /v1/branded-calling/enterprises/{id} | Get a registered business |
| [**GetBrandedCallingIdentity**](BrandedCallingApi.md#getbrandedcallingidentity) | **GET** /v1/branded-calling/identities/{id} | Get a caller identity |
| [**ListBrandedCallingCallReasons**](BrandedCallingApi.md#listbrandedcallingcallreasons) | **GET** /v1/branded-calling/call-reasons | List pre-approved call reasons |
| [**ListBrandedCallingEnterprises**](BrandedCallingApi.md#listbrandedcallingenterprises) | **GET** /v1/branded-calling/enterprises | List registered businesses |
| [**ListBrandedCallingIdentities**](BrandedCallingApi.md#listbrandedcallingidentities) | **GET** /v1/branded-calling/identities | List caller identities |
| [**ListBrandedCallingIdentityNumbers**](BrandedCallingApi.md#listbrandedcallingidentitynumbers) | **GET** /v1/branded-calling/identities/{id}/numbers | List the numbers on a caller identity |
| [**PreflightBrandedCallingIdentity**](BrandedCallingApi.md#preflightbrandedcallingidentity) | **POST** /v1/branded-calling/identities/preflight | Dry-run a caller identity before creating it |
| [**ResendBrandedCallingAuthorizerCode**](BrandedCallingApi.md#resendbrandedcallingauthorizercode) | **POST** /v1/branded-calling/identities/{id}/verify-email | Resend the authorizer&#39;s code |
| [**ShareBrandedCallingIdentityForm**](BrandedCallingApi.md#sharebrandedcallingidentityform) | **POST** /v1/branded-calling/share | Create a caller identity share link |
| [**UpdateBrandedCallingIdentity**](BrandedCallingApi.md#updatebrandedcallingidentity) | **PATCH** /v1/branded-calling/identities/{id} | Edit or resubmit a caller identity |

<a id="attachbrandedcallingnumbers"></a>
# **AttachBrandedCallingNumbers**
> ListBrandedCallingIdentityNumbers200Response AttachBrandedCallingNumbers (string id, AttachBrandedCallingNumbersRequest attachBrandedCallingNumbersRequest)

Attach numbers to a verified identity

Files a Letter of Authorization signed by you (Zernio is named as the authorized agent managing the numbers) and opens a vetting batch of up to 15 US numbers you own. The batch is all-or-nothing: one ineligible number refuses the whole call. Each number shows the identity once its own status reaches `verified`. A number belongs to one identity at a time. 

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
    public class AttachBrandedCallingNumbersExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var attachBrandedCallingNumbersRequest = new AttachBrandedCallingNumbersRequest(); // AttachBrandedCallingNumbersRequest | 

            try
            {
                // Attach numbers to a verified identity
                ListBrandedCallingIdentityNumbers200Response result = apiInstance.AttachBrandedCallingNumbers(id, attachBrandedCallingNumbersRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.AttachBrandedCallingNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AttachBrandedCallingNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Attach numbers to a verified identity
    ApiResponse<ListBrandedCallingIdentityNumbers200Response> response = apiInstance.AttachBrandedCallingNumbersWithHttpInfo(id, attachBrandedCallingNumbersRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.AttachBrandedCallingNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **attachBrandedCallingNumbersRequest** | [**AttachBrandedCallingNumbersRequest**](AttachBrandedCallingNumbersRequest.md) |  |  |

### Return type

[**ListBrandedCallingIdentityNumbers200Response**](ListBrandedCallingIdentityNumbers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Batch opened. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity or phone number not found |  -  |
| **409** | The identity is not verified yet, or a number already belongs to an identity (code invalid_resource_state). |  -  |
| **422** | A number is not a US number or not active, or the carrier refused the batch (the message names the number). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="confirmbrandedcallingauthorizeremail"></a>
# **ConfirmBrandedCallingAuthorizerEmail**
> BrandedCallingIdentity ConfirmBrandedCallingAuthorizerEmail (string id, ConfirmBrandedCallingAuthorizerEmailRequest confirmBrandedCallingAuthorizerEmailRequest)

Confirm the authorizer's code

The last customer step. On success the stored references are filed and the identity is submitted to carrier vetting in the same call (`in_review`). If a later step fails the identity stays `pending_email_verification` with the email already verified; calling again resumes from that step. 

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
    public class ConfirmBrandedCallingAuthorizerEmailExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var confirmBrandedCallingAuthorizerEmailRequest = new ConfirmBrandedCallingAuthorizerEmailRequest(); // ConfirmBrandedCallingAuthorizerEmailRequest | 

            try
            {
                // Confirm the authorizer's code
                BrandedCallingIdentity result = apiInstance.ConfirmBrandedCallingAuthorizerEmail(id, confirmBrandedCallingAuthorizerEmailRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.ConfirmBrandedCallingAuthorizerEmail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConfirmBrandedCallingAuthorizerEmailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Confirm the authorizer's code
    ApiResponse<BrandedCallingIdentity> response = apiInstance.ConfirmBrandedCallingAuthorizerEmailWithHttpInfo(id, confirmBrandedCallingAuthorizerEmailRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.ConfirmBrandedCallingAuthorizerEmailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **confirmBrandedCallingAuthorizerEmailRequest** | [**ConfirmBrandedCallingAuthorizerEmailRequest**](ConfirmBrandedCallingAuthorizerEmailRequest.md) |  |  |

### Return type

[**BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The identity, now in carrier vetting. |  -  |
| **400** | The code is wrong or expired (param code), or the body is invalid. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity not found |  -  |
| **409** | The identity is not waiting for a code (code invalid_resource_state). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbrandedcallingenterprise"></a>
# **CreateBrandedCallingEnterprise**
> BrandedCallingEnterprise CreateBrandedCallingEnterprise (CreateBrandedCallingEnterpriseRequest createBrandedCallingEnterpriseRequest, string? idempotencyKey = null)

Register a business for Branded Calling

Stores the legal entity behind your caller identities. Nothing is filed with the carrier until the business's first identity passes review. Only businesses registered in the US or Canada qualify (a FEIN or Canadian equivalent is required); any other country returns `422`. Send an `Idempotency-Key` so a retry replays the original response instead of registering the business twice. 

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
    public class CreateBrandedCallingEnterpriseExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var createBrandedCallingEnterpriseRequest = new CreateBrandedCallingEnterpriseRequest(); // CreateBrandedCallingEnterpriseRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Register a business for Branded Calling
                BrandedCallingEnterprise result = apiInstance.CreateBrandedCallingEnterprise(createBrandedCallingEnterpriseRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.CreateBrandedCallingEnterprise: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBrandedCallingEnterpriseWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Register a business for Branded Calling
    ApiResponse<BrandedCallingEnterprise> response = apiInstance.CreateBrandedCallingEnterpriseWithHttpInfo(createBrandedCallingEnterpriseRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.CreateBrandedCallingEnterpriseWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createBrandedCallingEnterpriseRequest** | [**CreateBrandedCallingEnterpriseRequest**](CreateBrandedCallingEnterpriseRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**BrandedCallingEnterprise**](BrandedCallingEnterprise.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Business stored. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | The business is not registered in the US or Canada (code feature_not_available), or the Idempotency-Key was reused with a different body (code idempotency_key_reused). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbrandedcallingidentity"></a>
# **CreateBrandedCallingIdentity**
> BrandedCallingIdentity CreateBrandedCallingIdentity (CreateBrandedCallingIdentityRequest createBrandedCallingIdentityRequest, string? idempotencyKey = null)

Create a caller identity

A caller identity is what the callee sees: display name, logo and call reasons, backed by a registered business and three references the carrier vetting team phones. It starts in Zernio review (`requested`). Once approved, the carrier emails the authorizer a 6-digit code; confirm it with the verify-email endpoint and the identity goes into carrier vetting on its own. Track it with `GET` or the `branded_calling.identity.status_updated` webhook.  Billing: $100 per identity per month while it is verified. The first month is charged when the carrier verifies the identity, never when it is filed: nothing is charged while it is in our review or carrier vetting, or if it is rejected. An edit that sends a verified identity back to vetting pauses the fee until it is verified again. Branded calls add $0.10 each, counted on every outbound call from a verified branded number to a US destination (whether or not the callee's carrier displayed the branding); the surcharge shows as `brandedCallUSD` on the call's billing and in `GET /v1/voice/calls/estimate` when you pass `from`.  Run `POST /v1/branded-calling/identities/preflight` with the same body first to catch what the review would bounce. Send an `Idempotency-Key` so a retry replays the original response instead of creating a second identity. 

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
    public class CreateBrandedCallingIdentityExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var createBrandedCallingIdentityRequest = new CreateBrandedCallingIdentityRequest(); // CreateBrandedCallingIdentityRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Create a caller identity
                BrandedCallingIdentity result = apiInstance.CreateBrandedCallingIdentity(createBrandedCallingIdentityRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.CreateBrandedCallingIdentity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBrandedCallingIdentityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a caller identity
    ApiResponse<BrandedCallingIdentity> response = apiInstance.CreateBrandedCallingIdentityWithHttpInfo(createBrandedCallingIdentityRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.CreateBrandedCallingIdentityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createBrandedCallingIdentityRequest** | [**CreateBrandedCallingIdentityRequest**](CreateBrandedCallingIdentityRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Identity created, in review. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Usage-based billing is required (code usage_billing_required). |  -  |
| **404** | Business not found |  -  |
| **409** | Same Idempotency-Key still processing; retry after a short backoff |  -  |
| **422** | The logo could not be downloaded or is not an image, or the Idempotency-Key was reused with a different body (code idempotency_key_reused). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebrandedcallingenterprise"></a>
# **DeleteBrandedCallingEnterprise**
> DeleteBrandedCallingEnterprise200Response DeleteBrandedCallingEnterprise (string id)

Delete a registered business

Refused while the business still has caller identities (delete those first).

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
    public class DeleteBrandedCallingEnterpriseExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Delete a registered business
                DeleteBrandedCallingEnterprise200Response result = apiInstance.DeleteBrandedCallingEnterprise(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.DeleteBrandedCallingEnterprise: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBrandedCallingEnterpriseWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a registered business
    ApiResponse<DeleteBrandedCallingEnterprise200Response> response = apiInstance.DeleteBrandedCallingEnterpriseWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.DeleteBrandedCallingEnterpriseWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**DeleteBrandedCallingEnterprise200Response**](DeleteBrandedCallingEnterprise200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Business not found |  -  |
| **409** | The business still has caller identities (code invalid_resource_state). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebrandedcallingidentity"></a>
# **DeleteBrandedCallingIdentity**
> DeleteBrandedCallingEnterprise200Response DeleteBrandedCallingIdentity (string id)

Delete a caller identity

Detaches its numbers and removes the identity at the carrier, which ends the monthly fee. Refused while an infringement claim is open.

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
    public class DeleteBrandedCallingIdentityExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Delete a caller identity
                DeleteBrandedCallingEnterprise200Response result = apiInstance.DeleteBrandedCallingIdentity(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.DeleteBrandedCallingIdentity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBrandedCallingIdentityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a caller identity
    ApiResponse<DeleteBrandedCallingEnterprise200Response> response = apiInstance.DeleteBrandedCallingIdentityWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.DeleteBrandedCallingIdentityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**DeleteBrandedCallingEnterprise200Response**](DeleteBrandedCallingEnterprise200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity not found |  -  |
| **409** | An infringement claim is open on this identity (code invalid_resource_state). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="detachbrandedcallingnumbers"></a>
# **DetachBrandedCallingNumbers**
> DetachBrandedCallingNumbers200Response DetachBrandedCallingNumbers (string id, DetachBrandedCallingNumbersRequest detachBrandedCallingNumbersRequest)

Detach numbers from an identity

Deregisters the numbers at the carrier and frees them for another identity. Up to 100 per call.

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
    public class DetachBrandedCallingNumbersExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var detachBrandedCallingNumbersRequest = new DetachBrandedCallingNumbersRequest(); // DetachBrandedCallingNumbersRequest | 

            try
            {
                // Detach numbers from an identity
                DetachBrandedCallingNumbers200Response result = apiInstance.DetachBrandedCallingNumbers(id, detachBrandedCallingNumbersRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.DetachBrandedCallingNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DetachBrandedCallingNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Detach numbers from an identity
    ApiResponse<DetachBrandedCallingNumbers200Response> response = apiInstance.DetachBrandedCallingNumbersWithHttpInfo(id, detachBrandedCallingNumbersRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.DetachBrandedCallingNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **detachBrandedCallingNumbersRequest** | [**DetachBrandedCallingNumbersRequest**](DetachBrandedCallingNumbersRequest.md) |  |  |

### Return type

[**DetachBrandedCallingNumbers200Response**](DetachBrandedCallingNumbers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Numbers detached. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity not found, or none of the numbers is attached to it |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbrandedcallingenterprise"></a>
# **GetBrandedCallingEnterprise**
> BrandedCallingEnterprise GetBrandedCallingEnterprise (string id)

Get a registered business

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
    public class GetBrandedCallingEnterpriseExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get a registered business
                BrandedCallingEnterprise result = apiInstance.GetBrandedCallingEnterprise(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.GetBrandedCallingEnterprise: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBrandedCallingEnterpriseWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a registered business
    ApiResponse<BrandedCallingEnterprise> response = apiInstance.GetBrandedCallingEnterpriseWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.GetBrandedCallingEnterpriseWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**BrandedCallingEnterprise**](BrandedCallingEnterprise.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The business. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Business not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbrandedcallingidentity"></a>
# **GetBrandedCallingIdentity**
> BrandedCallingIdentity GetBrandedCallingIdentity (string id)

Get a caller identity

Poll this for review and vetting progress, or subscribe to `branded_calling.identity.status_updated`.

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
    public class GetBrandedCallingIdentityExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get a caller identity
                BrandedCallingIdentity result = apiInstance.GetBrandedCallingIdentity(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.GetBrandedCallingIdentity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBrandedCallingIdentityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a caller identity
    ApiResponse<BrandedCallingIdentity> response = apiInstance.GetBrandedCallingIdentityWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.GetBrandedCallingIdentityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The identity with its numbers. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbrandedcallingcallreasons"></a>
# **ListBrandedCallingCallReasons**
> ListBrandedCallingCallReasons200Response ListBrandedCallingCallReasons ()

List pre-approved call reasons

The carrier catalogue of call reasons that pass vetting automatically. Any other wording is allowed on an identity but is vetted by hand.

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
    public class ListBrandedCallingCallReasonsExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);

            try
            {
                // List pre-approved call reasons
                ListBrandedCallingCallReasons200Response result = apiInstance.ListBrandedCallingCallReasons();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingCallReasons: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBrandedCallingCallReasonsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List pre-approved call reasons
    ApiResponse<ListBrandedCallingCallReasons200Response> response = apiInstance.ListBrandedCallingCallReasonsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingCallReasonsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListBrandedCallingCallReasons200Response**](ListBrandedCallingCallReasons200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The catalogue. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbrandedcallingenterprises"></a>
# **ListBrandedCallingEnterprises**
> ListBrandedCallingEnterprises200Response ListBrandedCallingEnterprises ()

List registered businesses

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
    public class ListBrandedCallingEnterprisesExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);

            try
            {
                // List registered businesses
                ListBrandedCallingEnterprises200Response result = apiInstance.ListBrandedCallingEnterprises();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingEnterprises: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBrandedCallingEnterprisesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List registered businesses
    ApiResponse<ListBrandedCallingEnterprises200Response> response = apiInstance.ListBrandedCallingEnterprisesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingEnterprisesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListBrandedCallingEnterprises200Response**](ListBrandedCallingEnterprises200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The workspace&#39;s businesses. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbrandedcallingidentities"></a>
# **ListBrandedCallingIdentities**
> ListBrandedCallingIdentities200Response ListBrandedCallingIdentities ()

List caller identities

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
    public class ListBrandedCallingIdentitiesExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);

            try
            {
                // List caller identities
                ListBrandedCallingIdentities200Response result = apiInstance.ListBrandedCallingIdentities();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingIdentities: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBrandedCallingIdentitiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List caller identities
    ApiResponse<ListBrandedCallingIdentities200Response> response = apiInstance.ListBrandedCallingIdentitiesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingIdentitiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListBrandedCallingIdentities200Response**](ListBrandedCallingIdentities200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The workspace&#39;s identities with their numbers. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbrandedcallingidentitynumbers"></a>
# **ListBrandedCallingIdentityNumbers**
> ListBrandedCallingIdentityNumbers200Response ListBrandedCallingIdentityNumbers (string id)

List the numbers on a caller identity

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
    public class ListBrandedCallingIdentityNumbersExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // List the numbers on a caller identity
                ListBrandedCallingIdentityNumbers200Response result = apiInstance.ListBrandedCallingIdentityNumbers(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingIdentityNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBrandedCallingIdentityNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List the numbers on a caller identity
    ApiResponse<ListBrandedCallingIdentityNumbers200Response> response = apiInstance.ListBrandedCallingIdentityNumbersWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.ListBrandedCallingIdentityNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ListBrandedCallingIdentityNumbers200Response**](ListBrandedCallingIdentityNumbers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Attached numbers with their vetting status. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="preflightbrandedcallingidentity"></a>
# **PreflightBrandedCallingIdentity**
> PreflightBrandedCallingIdentity200Response PreflightBrandedCallingIdentity (PreflightBrandedCallingIdentityRequest preflightBrandedCallingIdentityRequest)

Dry-run a caller identity before creating it

Validates the exact body `POST /v1/branded-calling/identities` takes and runs the same deterministic lints the review runs on it without creating anything, with the same codes and fields the queued identity's findings carry. A `block` finding is what the review would bounce (two references sharing a phone, a reference inside the business, an invalid timezone); a `warn` finding slows vetting (a display name that does not read as the business, a call reason outside the carrier catalogue, a public-mailbox authorizer, a logo that does not answer). `ok` is true when there is no `block`. 

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
    public class PreflightBrandedCallingIdentityExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var preflightBrandedCallingIdentityRequest = new PreflightBrandedCallingIdentityRequest(); // PreflightBrandedCallingIdentityRequest | 

            try
            {
                // Dry-run a caller identity before creating it
                PreflightBrandedCallingIdentity200Response result = apiInstance.PreflightBrandedCallingIdentity(preflightBrandedCallingIdentityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.PreflightBrandedCallingIdentity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreflightBrandedCallingIdentityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Dry-run a caller identity before creating it
    ApiResponse<PreflightBrandedCallingIdentity200Response> response = apiInstance.PreflightBrandedCallingIdentityWithHttpInfo(preflightBrandedCallingIdentityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.PreflightBrandedCallingIdentityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **preflightBrandedCallingIdentityRequest** | [**PreflightBrandedCallingIdentityRequest**](PreflightBrandedCallingIdentityRequest.md) |  |  |

### Return type

[**PreflightBrandedCallingIdentity200Response**](PreflightBrandedCallingIdentity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The findings; nothing was created. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Business not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="resendbrandedcallingauthorizercode"></a>
# **ResendBrandedCallingAuthorizerCode**
> ResendBrandedCallingAuthorizerCode200Response ResendBrandedCallingAuthorizerCode (string id)

Resend the authorizer's code

Emails the authorizer a fresh 6-digit code (the previous one stops working). Only while the identity is `pending_email_verification`.

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
    public class ResendBrandedCallingAuthorizerCodeExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Resend the authorizer's code
                ResendBrandedCallingAuthorizerCode200Response result = apiInstance.ResendBrandedCallingAuthorizerCode(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.ResendBrandedCallingAuthorizerCode: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResendBrandedCallingAuthorizerCodeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resend the authorizer's code
    ApiResponse<ResendBrandedCallingAuthorizerCode200Response> response = apiInstance.ResendBrandedCallingAuthorizerCodeWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.ResendBrandedCallingAuthorizerCodeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ResendBrandedCallingAuthorizerCode200Response**](ResendBrandedCallingAuthorizerCode200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Code sent. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity not found |  -  |
| **409** | The identity is not waiting for a code (code invalid_resource_state). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sharebrandedcallingidentityform"></a>
# **ShareBrandedCallingIdentityForm**
> ShareBrandedCallingIdentityForm200Response ShareBrandedCallingIdentityForm (ShareBrandedCallingIdentityFormRequest? shareBrandedCallingIdentityFormRequest = null)

Create a caller identity share link

Creates a single-use link (valid 7 days) where the end business fills in the caller identity itself, with no Zernio login: display name, logo, call reasons, the authorizer and the three references. What it submits lands under your team as `requested`, the same review as an API submission, and `branded_calling.identity.status_updated` fires. Scope the link with `identityId` (complete an identity that is `requested` or `changes_requested`), with `enterpriseId` (a new identity for a registered business), or with neither (the business registers itself and its first identity). The person opening the link can forward a fresh one to someone else, which retires theirs. 

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
    public class ShareBrandedCallingIdentityFormExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var shareBrandedCallingIdentityFormRequest = new ShareBrandedCallingIdentityFormRequest?(); // ShareBrandedCallingIdentityFormRequest? |  (optional) 

            try
            {
                // Create a caller identity share link
                ShareBrandedCallingIdentityForm200Response result = apiInstance.ShareBrandedCallingIdentityForm(shareBrandedCallingIdentityFormRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.ShareBrandedCallingIdentityForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ShareBrandedCallingIdentityFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a caller identity share link
    ApiResponse<ShareBrandedCallingIdentityForm200Response> response = apiInstance.ShareBrandedCallingIdentityFormWithHttpInfo(shareBrandedCallingIdentityFormRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.ShareBrandedCallingIdentityFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shareBrandedCallingIdentityFormRequest** | [**ShareBrandedCallingIdentityFormRequest?**](ShareBrandedCallingIdentityFormRequest?.md) |  | [optional]  |

### Return type

[**ShareBrandedCallingIdentityForm200Response**](ShareBrandedCallingIdentityForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Share link created. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Business or identity not found, or the identity is not in review |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebrandedcallingidentity"></a>
# **UpdateBrandedCallingIdentity**
> BrandedCallingIdentity UpdateBrandedCallingIdentity (string id, UpdateBrandedCallingIdentityRequest updateBrandedCallingIdentityRequest)

Edit or resubmit a caller identity

Allowed while the identity is `requested`, `changes_requested` or `rejected`. Answering a change request (send `reviewAnswers` keyed by point id, and any edited fields) puts it back in review. On a carrier rejection the edits are applied at the carrier and the identity is resubmitted straight away. 

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
    public class UpdateBrandedCallingIdentityExample
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
            var apiInstance = new BrandedCallingApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var updateBrandedCallingIdentityRequest = new UpdateBrandedCallingIdentityRequest(); // UpdateBrandedCallingIdentityRequest | 

            try
            {
                // Edit or resubmit a caller identity
                BrandedCallingIdentity result = apiInstance.UpdateBrandedCallingIdentity(id, updateBrandedCallingIdentityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandedCallingApi.UpdateBrandedCallingIdentity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBrandedCallingIdentityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Edit or resubmit a caller identity
    ApiResponse<BrandedCallingIdentity> response = apiInstance.UpdateBrandedCallingIdentityWithHttpInfo(id, updateBrandedCallingIdentityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandedCallingApi.UpdateBrandedCallingIdentityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **updateBrandedCallingIdentityRequest** | [**UpdateBrandedCallingIdentityRequest**](UpdateBrandedCallingIdentityRequest.md) |  |  |

### Return type

[**BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated identity. |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Identity not found |  -  |
| **409** | The identity cannot be edited in its current status (code invalid_resource_state). |  -  |
| **422** | reviewAnswers names a point id that is not on the open change request, or there is no open request (code invalid_field_value, param reviewAnswers). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

