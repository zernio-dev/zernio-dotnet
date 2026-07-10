# Zernio.Api.PhoneNumbersApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelPhoneNumberPortIn**](PhoneNumbersApi.md#cancelphonenumberportin) | **DELETE** /v1/phone-numbers/port-in/{id} | Cancel a port-in |
| [**CheckPhoneNumberAvailability**](PhoneNumbersApi.md#checkphonenumberavailability) | **GET** /v1/phone-numbers/availability | Check country availability |
| [**CheckPhoneNumberPortability**](PhoneNumbersApi.md#checkphonenumberportability) | **POST** /v1/phone-numbers/port-in/check | Check portability |
| [**CreatePhoneNumberKycLink**](PhoneNumbersApi.md#createphonenumberkyclink) | **POST** /v1/phone-numbers/kyc/share | Create a hosted KYC link |
| [**CreatePhoneNumberPortIn**](PhoneNumbersApi.md#createphonenumberportin) | **POST** /v1/phone-numbers/port-in | Port numbers in |
| [**GetPhoneNumber**](PhoneNumbersApi.md#getphonenumber) | **GET** /v1/phone-numbers/{id} | Get phone number |
| [**GetPhoneNumberKycForm**](PhoneNumbersApi.md#getphonenumberkycform) | **GET** /v1/phone-numbers/kyc | Get KYC form spec |
| [**GetPhoneNumberRemediation**](PhoneNumbersApi.md#getphonenumberremediation) | **GET** /v1/phone-numbers/{id}/remediate | Get declined requirements |
| [**ListPhoneNumberCountries**](PhoneNumbersApi.md#listphonenumbercountries) | **GET** /v1/phone-numbers/countries | List offerable number countries |
| [**ListPhoneNumberPortIns**](PhoneNumbersApi.md#listphonenumberportins) | **GET** /v1/phone-numbers/port-in | List port-in orders |
| [**ListPhoneNumbers**](PhoneNumbersApi.md#listphonenumbers) | **GET** /v1/phone-numbers | List phone numbers |
| [**PurchasePhoneNumber**](PhoneNumbersApi.md#purchasephonenumber) | **POST** /v1/phone-numbers/purchase | Purchase phone number |
| [**ReleasePhoneNumber**](PhoneNumbersApi.md#releasephonenumber) | **DELETE** /v1/phone-numbers/{id} | Release phone number |
| [**RemediatePhoneNumber**](PhoneNumbersApi.md#remediatephonenumber) | **POST** /v1/phone-numbers/{id}/remediate | Resubmit a declined number |
| [**ReviewPhoneNumberKycPacket**](PhoneNumbersApi.md#reviewphonenumberkycpacket) | **POST** /v1/phone-numbers/kyc/review-packet | Pre-review a KYC packet |
| [**SearchAvailablePhoneNumbers**](PhoneNumbersApi.md#searchavailablephonenumbers) | **GET** /v1/phone-numbers/available | Search available numbers |
| [**SubmitPhoneNumberKyc**](PhoneNumbersApi.md#submitphonenumberkyc) | **POST** /v1/phone-numbers/kyc | Submit KYC |
| [**UploadPhoneNumberKycDocument**](PhoneNumbersApi.md#uploadphonenumberkycdocument) | **POST** /v1/phone-numbers/kyc/upload-document | Upload a KYC document |
| [**UploadPhoneNumberPortInDocument**](PhoneNumbersApi.md#uploadphonenumberportindocument) | **POST** /v1/phone-numbers/port-in/documents | Upload a porting document |
| [**ValidatePhoneNumberKycAddress**](PhoneNumbersApi.md#validatephonenumberkycaddress) | **POST** /v1/phone-numbers/kyc/validate-address | Pre-validate KYC address |

<a id="cancelphonenumberportin"></a>
# **CancelPhoneNumberPortIn**
> CancelPhoneNumberPortIn200Response CancelPhoneNumberPortIn (string id)

Cancel a port-in

Cancel an in-flight port (wrong number, staying with the old carrier). Only orders that haven't ported can be cancelled; a completed port is a normal number release instead. The carrier may report `cancel-pending` briefly while the losing carrier acknowledges; it settles to `cancelled`. 

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
    public class CancelPhoneNumberPortInExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | Porting order ID (from the port-in list).

            try
            {
                // Cancel a port-in
                CancelPhoneNumberPortIn200Response result = apiInstance.CancelPhoneNumberPortIn(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.CancelPhoneNumberPortIn: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelPhoneNumberPortInWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel a port-in
    ApiResponse<CancelPhoneNumberPortIn200Response> response = apiInstance.CancelPhoneNumberPortInWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.CancelPhoneNumberPortInWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Porting order ID (from the port-in list). |  |

### Return type

[**CancelPhoneNumberPortIn200Response**](CancelPhoneNumberPortIn200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cancel accepted (idempotent when already cancelled). |  -  |
| **401** | Unauthorized |  -  |
| **404** | Porting order not found |  -  |
| **409** | Port already completed (release the number instead), or the carrier rejected the cancel (reason included) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkphonenumberavailability"></a>
# **CheckPhoneNumberAvailability**
> CheckPhoneNumberAvailability200Response CheckPhoneNumberAvailability (string country)

Check country availability

Pre-purchase check, so you can warn BEFORE a customer invests in KYC (regulated review is async, 1-3 days). Tells you whether we have deliverable inventory, and what address the customer needs:   - `addressConstraint: geo`  → the registered address MUST be in one of     the returned `areas` (the only place we have stock). A different-area     address passes pre-approval but the number can never be assigned.   - `addressConstraint: country` → any in-country address works.   - `addressConstraint: none` → field-only / instant country, no address. Call this before starting the KYC form for regulated countries. 

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
    public class CheckPhoneNumberAvailabilityExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var country = "country_example";  // string | ISO-2 country code.

            try
            {
                // Check country availability
                CheckPhoneNumberAvailability200Response result = apiInstance.CheckPhoneNumberAvailability(country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.CheckPhoneNumberAvailability: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckPhoneNumberAvailabilityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check country availability
    ApiResponse<CheckPhoneNumberAvailability200Response> response = apiInstance.CheckPhoneNumberAvailabilityWithHttpInfo(country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.CheckPhoneNumberAvailabilityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **country** | **string** | ISO-2 country code. |  |

### Return type

[**CheckPhoneNumberAvailability200Response**](CheckPhoneNumberAvailability200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Availability + address constraint. |  -  |
| **400** | Country not offerable |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkphonenumberportability"></a>
# **CheckPhoneNumberPortability**
> CheckPhoneNumberPortability200Response CheckPhoneNumberPortability (CheckPhoneNumberPortabilityRequest checkPhoneNumberPortabilityRequest)

Check portability

Pre-flight portability check: whether each number can be ported in and whether it qualifies for FastPort, BEFORE the user commits to a port order (LOA, invoice, service address). Read-only; creates no order and bills nothing. 

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
    public class CheckPhoneNumberPortabilityExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var checkPhoneNumberPortabilityRequest = new CheckPhoneNumberPortabilityRequest(); // CheckPhoneNumberPortabilityRequest | 

            try
            {
                // Check portability
                CheckPhoneNumberPortability200Response result = apiInstance.CheckPhoneNumberPortability(checkPhoneNumberPortabilityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.CheckPhoneNumberPortability: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckPhoneNumberPortabilityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check portability
    ApiResponse<CheckPhoneNumberPortability200Response> response = apiInstance.CheckPhoneNumberPortabilityWithHttpInfo(checkPhoneNumberPortabilityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.CheckPhoneNumberPortabilityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **checkPhoneNumberPortabilityRequest** | [**CheckPhoneNumberPortabilityRequest**](CheckPhoneNumberPortabilityRequest.md) |  |  |

### Return type

[**CheckPhoneNumberPortability200Response**](CheckPhoneNumberPortability200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-number portability. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createphonenumberkyclink"></a>
# **CreatePhoneNumberKycLink**
> CreatePhoneNumberKycLink200Response CreatePhoneNumberKycLink (CreatePhoneNumberKycLinkRequest createPhoneNumberKycLinkRequest)

Create a hosted KYC link

Create a single-use, 7-day hosted KYC link that your end customer completes WITHOUT a Zernio login — useful when the person who holds the ID and address is not your team. They fill the regulated verification on a Zernio-hosted page; the number provisions under YOUR account once they submit. Only regulated (KYC) countries are valid: a country that does not require KYC returns 400.  White-label the page with `branding` (your company name, logo, brand color). Supply `redirect_url` to send the end customer back to your own site after a successful submit (completion params are appended — see below). Listen for the `whatsapp.number.kyc_submitted` webhook to react when the form is completed. 

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
    public class CreatePhoneNumberKycLinkExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var createPhoneNumberKycLinkRequest = new CreatePhoneNumberKycLinkRequest(); // CreatePhoneNumberKycLinkRequest | 

            try
            {
                // Create a hosted KYC link
                CreatePhoneNumberKycLink200Response result = apiInstance.CreatePhoneNumberKycLink(createPhoneNumberKycLinkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.CreatePhoneNumberKycLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreatePhoneNumberKycLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a hosted KYC link
    ApiResponse<CreatePhoneNumberKycLink200Response> response = apiInstance.CreatePhoneNumberKycLinkWithHttpInfo(createPhoneNumberKycLinkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.CreatePhoneNumberKycLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createPhoneNumberKycLinkRequest** | [**CreatePhoneNumberKycLinkRequest**](CreatePhoneNumberKycLinkRequest.md) |  |  |

### Return type

[**CreatePhoneNumberKycLink200Response**](CreatePhoneNumberKycLink200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hosted KYC link created. |  -  |
| **400** | Country does not require KYC (not a regulated country). |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createphonenumberportin"></a>
# **CreatePhoneNumberPortIn**
> CreatePhoneNumberPortIn201Response CreatePhoneNumberPortIn (CreatePhoneNumberPortInRequest createPhoneNumberPortInRequest)

Port numbers in

Submit a port-in for one or more existing numbers from another carrier. Creates the carrier order(s), attaches the end-user (current account) info plus the LOA and invoice documents, and submits to the losing carrier. The transfer PIN is forwarded to the carrier and never stored. Ported numbers arrive voice-ready (and SMS-ready where the order supports messaging).  Run the portability check (POST /v1/phone-numbers/port-in/check) and upload the two documents (POST /v1/phone-numbers/port-in/documents) first. The carrier may split the numbers into several orders (by country, number type, losing carrier); `orders` carries per-order results, and a partial failure still returns 201 with the failed orders' `error` set (they stay as cancellable drafts). 

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
    public class CreatePhoneNumberPortInExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var createPhoneNumberPortInRequest = new CreatePhoneNumberPortInRequest(); // CreatePhoneNumberPortInRequest | 

            try
            {
                // Port numbers in
                CreatePhoneNumberPortIn201Response result = apiInstance.CreatePhoneNumberPortIn(createPhoneNumberPortInRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.CreatePhoneNumberPortIn: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreatePhoneNumberPortInWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Port numbers in
    ApiResponse<CreatePhoneNumberPortIn201Response> response = apiInstance.CreatePhoneNumberPortInWithHttpInfo(createPhoneNumberPortInRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.CreatePhoneNumberPortInWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createPhoneNumberPortInRequest** | [**CreatePhoneNumberPortInRequest**](CreatePhoneNumberPortInRequest.md) |  |  |

### Return type

[**CreatePhoneNumberPortIn201Response**](CreatePhoneNumberPortIn201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Port submitted. Top-level fields mirror the first successfully submitted order; per-order truth (including failures) is in &#x60;orders&#x60;. |  -  |
| **401** | Unauthorized |  -  |
| **409** | A number is already provisioned, or already in an in-flight port |  -  |
| **422** | A number is not portable (reason included), or every split order failed to submit |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getphonenumber"></a>
# **GetPhoneNumber**
> GetPhoneNumber200Response GetPhoneNumber (string id)

Get phone number

Retrieve the current status of a purchased phone number. Poll this to track Meta pre-verification (US sync path) and, for regulated (Tier 3/4) numbers, the async lifecycle: pending_regulatory → active (or regulatory_declined). When a regulated number has an Onfido ID step, `onfidoVerificationUrl` appears here once the order is placed — forward it to the end user. (Or subscribe to the whatsapp.number.* webhooks instead of polling.) 

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
    public class GetPhoneNumberExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | Phone number record ID

            try
            {
                // Get phone number
                GetPhoneNumber200Response result = apiInstance.GetPhoneNumber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.GetPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get phone number
    ApiResponse<GetPhoneNumber200Response> response = apiInstance.GetPhoneNumberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.GetPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Phone number record ID |  |

### Return type

[**GetPhoneNumber200Response**](GetPhoneNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Phone number retrieved successfully |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getphonenumberkycform"></a>
# **GetPhoneNumberKycForm**
> GetPhoneNumberKycForm200Response GetPhoneNumberKycForm (string country)

Get KYC form spec

For a Tier 3/4 country, the fields the end customer must provide (Telnyx regulatory requirements) before a number can be ordered: text, date, address, or file (document) per requirement. 

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
    public class GetPhoneNumberKycFormExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var country = "country_example";  // string | 

            try
            {
                // Get KYC form spec
                GetPhoneNumberKycForm200Response result = apiInstance.GetPhoneNumberKycForm(country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.GetPhoneNumberKycForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPhoneNumberKycFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get KYC form spec
    ApiResponse<GetPhoneNumberKycForm200Response> response = apiInstance.GetPhoneNumberKycFormWithHttpInfo(country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.GetPhoneNumberKycFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **country** | **string** |  |  |

### Return type

[**GetPhoneNumberKycForm200Response**](GetPhoneNumberKycForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The KYC form spec. |  -  |
| **400** | Country not available |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getphonenumberremediation"></a>
# **GetPhoneNumberRemediation**
> GetPhoneNumberRemediation200Response GetPhoneNumberRemediation (string id)

Get declined requirements

For a number in `regulatory_declined`, returns ONLY the requirements the reviewer flagged declined, as a form spec (same shape as the KYC form GET). The customer fixes just those — Telnyx supports correcting a declined requirement group and re-submitting it (no new number/group). Falls back to the full spec if the provider exposes no per-requirement flags. 

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
    public class GetPhoneNumberRemediationExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | Phone number record ID.

            try
            {
                // Get declined requirements
                GetPhoneNumberRemediation200Response result = apiInstance.GetPhoneNumberRemediation(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.GetPhoneNumberRemediation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPhoneNumberRemediationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get declined requirements
    ApiResponse<GetPhoneNumberRemediation200Response> response = apiInstance.GetPhoneNumberRemediationWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.GetPhoneNumberRemediationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Phone number record ID. |  |

### Return type

[**GetPhoneNumberRemediation200Response**](GetPhoneNumberRemediation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The declined requirements to fix. |  -  |
| **400** | Number is not awaiting remediation |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listphonenumbercountries"></a>
# **ListPhoneNumberCountries**
> ListPhoneNumberCountries200Response ListPhoneNumberCountries ()

List offerable number countries

The phone number countries available to purchase, each with its flat monthly price (cents), regulatory tier, whether it needs end-user KYC (Tier 3/4), and per-feature availability (PSTN calls, WhatsApp, SMS, and WhatsApp Business Calling outbound). Drives the country picker. Tier-4 countries appear only when enabled. 

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
    public class ListPhoneNumberCountriesExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);

            try
            {
                // List offerable number countries
                ListPhoneNumberCountries200Response result = apiInstance.ListPhoneNumberCountries();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.ListPhoneNumberCountries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPhoneNumberCountriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List offerable number countries
    ApiResponse<ListPhoneNumberCountries200Response> response = apiInstance.ListPhoneNumberCountriesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.ListPhoneNumberCountriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListPhoneNumberCountries200Response**](ListPhoneNumberCountries200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Offerable countries, cheapest first. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listphonenumberportins"></a>
# **ListPhoneNumberPortIns**
> ListPhoneNumberPortIns200Response ListPhoneNumberPortIns ()

List port-in orders

Your porting orders, newest first (max 50). Poll this for port progress: pending, confirmed FOC date, exception reason, or ported. 

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
    public class ListPhoneNumberPortInsExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);

            try
            {
                // List port-in orders
                ListPhoneNumberPortIns200Response result = apiInstance.ListPhoneNumberPortIns();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.ListPhoneNumberPortIns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPhoneNumberPortInsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List port-in orders
    ApiResponse<ListPhoneNumberPortIns200Response> response = apiInstance.ListPhoneNumberPortInsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.ListPhoneNumberPortInsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListPhoneNumberPortIns200Response**](ListPhoneNumberPortIns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Porting orders |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listphonenumbers"></a>
# **ListPhoneNumbers**
> ListPhoneNumbers200Response ListPhoneNumbers (string? status = null, string? profileId = null)

List phone numbers

List all phone numbers purchased by the authenticated user. By default, released numbers are excluded. Connected (bring-your-own) WhatsApp numbers are returned in the separate `connected` array; they are not billed and have no provisioning lifecycle. 

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
    public class ListPhoneNumbersExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var status = "provisioning";  // string? | Filter by status (by default excludes released numbers). NOTE: `status=pending_regulatory` returns the \"provisioning\" view — numbers still in review PLUS recently-declined (last 30 days) ones, so a failed registration surfaces (with `regulatoryDeclineReason`) instead of silently disappearing. Declined numbers can be re-submitted via POST /v1/phone-numbers/{id}/remediate. `verifying` is the short-lived state after the number is provisioned on our side while WhatsApp confirms the activation code; the number is not billed until it reaches `active`.  (optional) 
            var profileId = "profileId_example";  // string? | Filter by profile (optional) 

            try
            {
                // List phone numbers
                ListPhoneNumbers200Response result = apiInstance.ListPhoneNumbers(status, profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.ListPhoneNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPhoneNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List phone numbers
    ApiResponse<ListPhoneNumbers200Response> response = apiInstance.ListPhoneNumbersWithHttpInfo(status, profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.ListPhoneNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string?** | Filter by status (by default excludes released numbers). NOTE: &#x60;status&#x3D;pending_regulatory&#x60; returns the \&quot;provisioning\&quot; view — numbers still in review PLUS recently-declined (last 30 days) ones, so a failed registration surfaces (with &#x60;regulatoryDeclineReason&#x60;) instead of silently disappearing. Declined numbers can be re-submitted via POST /v1/phone-numbers/{id}/remediate. &#x60;verifying&#x60; is the short-lived state after the number is provisioned on our side while WhatsApp confirms the activation code; the number is not billed until it reaches &#x60;active&#x60;.  | [optional]  |
| **profileId** | **string?** | Filter by profile | [optional]  |

### Return type

[**ListPhoneNumbers200Response**](ListPhoneNumbers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Phone numbers retrieved successfully |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="purchasephonenumber"></a>
# **PurchasePhoneNumber**
> PurchasePhoneNumber200Response PurchasePhoneNumber (PurchasePhoneNumberRequest purchasePhoneNumberRequest)

Purchase phone number

Payment-first: you do not pick a specific number, the system provisions one and auto-assigns it. With usage-based billing active and a payment method on file, the number provisions inline and bills per month on your usage-based invoice (there is no checkout redirect). No payment method on file returns `402 PAYMENT_REQUIRED`; a regulated country returns `202` with `status: \"kyc_required\"` and a `kycUrl`.  Requires usage-based billing (the Usage plan). The maximum number of phone numbers is determined by the user's plan. 

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
    public class PurchasePhoneNumberExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var purchasePhoneNumberRequest = new PurchasePhoneNumberRequest(); // PurchasePhoneNumberRequest | 

            try
            {
                // Purchase phone number
                PurchasePhoneNumber200Response result = apiInstance.PurchasePhoneNumber(purchasePhoneNumberRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.PurchasePhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PurchasePhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Purchase phone number
    ApiResponse<PurchasePhoneNumber200Response> response = apiInstance.PurchasePhoneNumberWithHttpInfo(purchasePhoneNumberRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.PurchasePhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchasePhoneNumberRequest** | [**PurchasePhoneNumberRequest**](PurchasePhoneNumberRequest.md) |  |  |

### Return type

[**PurchasePhoneNumber200Response**](PurchasePhoneNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Either a checkout URL (first number) or the provisioned phone number (subsequent numbers).  |  -  |
| **400** | Plan limit reached, profileId required, or country not available |  -  |
| **401** | Unauthorized |  -  |
| **403** | A paid plan is required |  -  |
| **409** | Duplicate-purchase protection: another number was purchased for this user within the last 10 minutes. Retry with allowMultiple: true to confirm the additional purchase is intentional.  |  -  |
| **202** | Country requires end-user KYC before the number can be ordered. |  -  |
| **402** | Payment method required (Metronome user with no card on file). Response body carries code: PAYMENT_REQUIRED; add a card, then retry. |  -  |
| **422** | International numbers require usage-based billing (legacy Stripe users are US-only). Response body code: USAGE_BILLING_REQUIRED. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="releasephonenumber"></a>
# **ReleasePhoneNumber**
> ReleasePhoneNumber200Response ReleasePhoneNumber (string id)

Release phone number

Release a purchased phone number. This will: 1. Disconnect any linked WhatsApp social account 2. Decrement the Stripe subscription quantity (or cancel if last number) 3. Release the number from Telnyx 4. Mark the number as released 

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
    public class ReleasePhoneNumberExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | Phone number record ID

            try
            {
                // Release phone number
                ReleasePhoneNumber200Response result = apiInstance.ReleasePhoneNumber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.ReleasePhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReleasePhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Release phone number
    ApiResponse<ReleasePhoneNumber200Response> response = apiInstance.ReleasePhoneNumberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.ReleasePhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Phone number record ID |  |

### Return type

[**ReleasePhoneNumber200Response**](ReleasePhoneNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Phone number released successfully |  -  |
| **400** | Phone number is already released or being released |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="remediatephonenumber"></a>
# **RemediatePhoneNumber**
> RemediatePhoneNumber200Response RemediatePhoneNumber (string id, RemediatePhoneNumberRequest remediatePhoneNumberRequest)

Resubmit a declined number

Submit corrected values/documents for the declined requirement(s). We PATCH them onto the SAME requirement group and re-submit it for approval; the number goes `regulatory_declined` → `pending_regulatory`. No new number and no new billing. Body shape matches the KYC submit (values / documents / address) — send only the corrected fields. 

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
    public class RemediatePhoneNumberExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var remediatePhoneNumberRequest = new RemediatePhoneNumberRequest(); // RemediatePhoneNumberRequest | 

            try
            {
                // Resubmit a declined number
                RemediatePhoneNumber200Response result = apiInstance.RemediatePhoneNumber(id, remediatePhoneNumberRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.RemediatePhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemediatePhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resubmit a declined number
    ApiResponse<RemediatePhoneNumber200Response> response = apiInstance.RemediatePhoneNumberWithHttpInfo(id, remediatePhoneNumberRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.RemediatePhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **remediatePhoneNumberRequest** | [**RemediatePhoneNumberRequest**](RemediatePhoneNumberRequest.md) |  |  |

### Return type

[**RemediatePhoneNumber200Response**](RemediatePhoneNumber200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Re-submitted for approval. |  -  |
| **400** | Number is not awaiting remediation / nothing to remediate |  -  |
| **401** | Unauthorized |  -  |
| **404** | Number not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reviewphonenumberkycpacket"></a>
# **ReviewPhoneNumberKycPacket**
> ReviewPhoneNumberKycPacket200Response ReviewPhoneNumberKycPacket (ReviewPhoneNumberKycPacketRequest reviewPhoneNumberKycPacketRequest)

Pre-review a KYC packet

Advisory dry-run of a regulated-KYC packet before submitting: reviews the exact documents the regulator will see (referenced by the ids from POST /v1/phone-numbers/kyc/upload-document) against the declared values and address, and returns plain-language advisories for likely decline reasons (wrong document type, mismatched address, one-sided ID scans). Non-blocking: advisories are warnings, submitting anyway is always allowed, and any review failure degrades to an empty list. 

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
    public class ReviewPhoneNumberKycPacketExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var reviewPhoneNumberKycPacketRequest = new ReviewPhoneNumberKycPacketRequest(); // ReviewPhoneNumberKycPacketRequest | 

            try
            {
                // Pre-review a KYC packet
                ReviewPhoneNumberKycPacket200Response result = apiInstance.ReviewPhoneNumberKycPacket(reviewPhoneNumberKycPacketRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.ReviewPhoneNumberKycPacket: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReviewPhoneNumberKycPacketWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pre-review a KYC packet
    ApiResponse<ReviewPhoneNumberKycPacket200Response> response = apiInstance.ReviewPhoneNumberKycPacketWithHttpInfo(reviewPhoneNumberKycPacketRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.ReviewPhoneNumberKycPacketWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **reviewPhoneNumberKycPacketRequest** | [**ReviewPhoneNumberKycPacketRequest**](ReviewPhoneNumberKycPacketRequest.md) |  |  |

### Return type

[**ReviewPhoneNumberKycPacket200Response**](ReviewPhoneNumberKycPacket200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Advisories (empty when the packet looks fine or the review was unavailable). |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="searchavailablephonenumbers"></a>
# **SearchAvailablePhoneNumbers**
> SearchAvailablePhoneNumbers200Response SearchAvailablePhoneNumbers (string? country = null, string? type = null, string? prefix = null, string? locality = null, string? contains = null, bool? sms = null, int? limit = null)

Search available numbers

Search the provider's inventory for numbers available to purchase in a country (default US). Optional filters narrow the results. The country must be offerable (see GET /v1/phone-numbers/countries). Voice capability is always required; pass `sms=true` to only see numbers that can also text (SMS support is per-number, not per-country). 

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
    public class SearchAvailablePhoneNumbersExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var country = "\"US\"";  // string? |  (optional)  (default to "US")
            var type = "type_example";  // string? | Number type; defaults to the country's WhatsApp-safe type (optional) 
            var prefix = "prefix_example";  // string? | Area code (optional) 
            var locality = "locality_example";  // string? | City (optional) 
            var contains = "contains_example";  // string? | Pattern to match within the number (optional) 
            var sms = true;  // bool? | true narrows the pool to SMS-capable numbers. Each result still carries its full `features` list for per-number capability badging. (optional) 
            var limit = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // Search available numbers
                SearchAvailablePhoneNumbers200Response result = apiInstance.SearchAvailablePhoneNumbers(country, type, prefix, locality, contains, sms, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.SearchAvailablePhoneNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchAvailablePhoneNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search available numbers
    ApiResponse<SearchAvailablePhoneNumbers200Response> response = apiInstance.SearchAvailablePhoneNumbersWithHttpInfo(country, type, prefix, locality, contains, sms, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.SearchAvailablePhoneNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **country** | **string?** |  | [optional] [default to &quot;US&quot;] |
| **type** | **string?** | Number type; defaults to the country&#39;s WhatsApp-safe type | [optional]  |
| **prefix** | **string?** | Area code | [optional]  |
| **locality** | **string?** | City | [optional]  |
| **contains** | **string?** | Pattern to match within the number | [optional]  |
| **sms** | **bool?** | true narrows the pool to SMS-capable numbers. Each result still carries its full &#x60;features&#x60; list for per-number capability badging. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 20] |

### Return type

[**SearchAvailablePhoneNumbers200Response**](SearchAvailablePhoneNumbers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Available numbers. |  -  |
| **400** | Country not available |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="submitphonenumberkyc"></a>
# **SubmitPhoneNumberKyc**
> SubmitPhoneNumberKyc200Response SubmitPhoneNumberKyc (SubmitPhoneNumberKycRequest submitPhoneNumberKycRequest)

Submit KYC

Submit the end customer's KYC (textual values, uploaded documents, address) for a Tier 3/4 country. Documents are streamed straight to the number provider and are not stored by Zernio. Builds + submits a regulatory requirement group and claims a pending_regulatory slot; the number is ordered + activated once the provider approves (asynchronous). A customer may hold several same-country numbers in review at once; a double-submit of the SAME attempt is deduped via `submissionId`.  For an ID-card document requirement, carriers commonly require BOTH sides: combine the front and back into a single file before uploading (the dashboard does this automatically). A one-sided ID is a common decline reason; fix it via POST /v1/phone-numbers/{id}/remediate.  Before submitting, call GET /v1/phone-numbers/availability to check the country has deliverable inventory and, for geographic-match countries, which area the address must be in — otherwise the submission can pass review yet never be assignable a number. 

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
    public class SubmitPhoneNumberKycExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var submitPhoneNumberKycRequest = new SubmitPhoneNumberKycRequest(); // SubmitPhoneNumberKycRequest | 

            try
            {
                // Submit KYC
                SubmitPhoneNumberKyc200Response result = apiInstance.SubmitPhoneNumberKyc(submitPhoneNumberKycRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.SubmitPhoneNumberKyc: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubmitPhoneNumberKycWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit KYC
    ApiResponse<SubmitPhoneNumberKyc200Response> response = apiInstance.SubmitPhoneNumberKycWithHttpInfo(submitPhoneNumberKycRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.SubmitPhoneNumberKycWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **submitPhoneNumberKycRequest** | [**SubmitPhoneNumberKycRequest**](SubmitPhoneNumberKycRequest.md) |  |  |

### Return type

[**SubmitPhoneNumberKyc200Response**](SubmitPhoneNumberKyc200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | KYC submitted (or already submitted); number pending review. |  -  |
| **400** | Validation error (e.g. address not in-country, file too large) |  -  |
| **409** | reuse requested but no prior approved verification exists for this country |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadphonenumberkycdocument"></a>
# **UploadPhoneNumberKycDocument**
> UploadPhoneNumberKycDocument200Response UploadPhoneNumberKycDocument (string xFilename, FileParameter body)

Upload a KYC document

Upload ONE document and get back its provider document id, to reference from POST /v1/phone-numbers/kyc via `documents[].documentId`. Send the RAW file bytes as the request body (not base64); put the filename in the `X-Filename` header. Uploading documents one-per-request keeps each request under the ~4.5MB body limit. The document streams straight to the number provider and is not stored by Zernio. 

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
    public class UploadPhoneNumberKycDocumentExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var xFilename = "xFilename_example";  // string | URL-encoded original filename.
            var body = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter | 

            try
            {
                // Upload a KYC document
                UploadPhoneNumberKycDocument200Response result = apiInstance.UploadPhoneNumberKycDocument(xFilename, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.UploadPhoneNumberKycDocument: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadPhoneNumberKycDocumentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload a KYC document
    ApiResponse<UploadPhoneNumberKycDocument200Response> response = apiInstance.UploadPhoneNumberKycDocumentWithHttpInfo(xFilename, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.UploadPhoneNumberKycDocumentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xFilename** | **string** | URL-encoded original filename. |  |
| **body** | **FileParameter****FileParameter** |  |  |

### Return type

[**UploadPhoneNumberKycDocument200Response**](UploadPhoneNumberKycDocument200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Document uploaded. |  -  |
| **400** | Missing X-Filename, empty body, or file too large (over 20MB). |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadphonenumberportindocument"></a>
# **UploadPhoneNumberPortInDocument**
> UploadPhoneNumberPortInDocument200Response UploadPhoneNumberPortInDocument (FileParameter file, string? kind = null)

Upload a porting document

Upload ONE porting document (the signed LOA or a recent carrier invoice) and get back its `documentId`, which the port-in create request takes as `loaDocumentId` / `invoiceDocumentId`. PDF, JPEG, or PNG, 10MB max. 

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
    public class UploadPhoneNumberPortInDocumentExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter | The document (PDF/JPEG/PNG, 10MB max).
            var kind = "loa";  // string? | Informational; used for the stored filename. (optional) 

            try
            {
                // Upload a porting document
                UploadPhoneNumberPortInDocument200Response result = apiInstance.UploadPhoneNumberPortInDocument(file, kind);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.UploadPhoneNumberPortInDocument: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadPhoneNumberPortInDocumentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload a porting document
    ApiResponse<UploadPhoneNumberPortInDocument200Response> response = apiInstance.UploadPhoneNumberPortInDocumentWithHttpInfo(file, kind);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.UploadPhoneNumberPortInDocumentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **file** | **FileParameter****FileParameter** | The document (PDF/JPEG/PNG, 10MB max). |  |
| **kind** | **string?** | Informational; used for the stored filename. | [optional]  |

### Return type

[**UploadPhoneNumberPortInDocument200Response**](UploadPhoneNumberPortInDocument200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Document uploaded. |  -  |
| **400** | Missing file, file too large, or unsupported type |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="validatephonenumberkycaddress"></a>
# **ValidatePhoneNumberKycAddress**
> ValidatePhoneNumberKycAddress200Response ValidatePhoneNumberKycAddress (ValidatePhoneNumberKycAddressRequest validatePhoneNumberKycAddressRequest)

Pre-validate KYC address

Optional early check for the address step of a Tier 4 (end-user identity) registration: validates a postal address for deliverability BEFORE the full KYC submit, so it can be corrected before any documents are uploaded. The full submit (POST /v1/phone-numbers/kyc) re-validates the address, so this call is purely a fast feedback path and skipping it is safe. Only the postal address is sent (no documents, no gov-ID fields). A region (`administrative_area`) is required by the validator; when it is omitted the pre-check is skipped and `{ ok: true, skipped: true }` is returned (the final submit still validates). 

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
    public class ValidatePhoneNumberKycAddressExample
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var validatePhoneNumberKycAddressRequest = new ValidatePhoneNumberKycAddressRequest(); // ValidatePhoneNumberKycAddressRequest | 

            try
            {
                // Pre-validate KYC address
                ValidatePhoneNumberKycAddress200Response result = apiInstance.ValidatePhoneNumberKycAddress(validatePhoneNumberKycAddressRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.ValidatePhoneNumberKycAddress: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ValidatePhoneNumberKycAddressWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pre-validate KYC address
    ApiResponse<ValidatePhoneNumberKycAddress200Response> response = apiInstance.ValidatePhoneNumberKycAddressWithHttpInfo(validatePhoneNumberKycAddressRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PhoneNumbersApi.ValidatePhoneNumberKycAddressWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **validatePhoneNumberKycAddressRequest** | [**ValidatePhoneNumberKycAddressRequest**](ValidatePhoneNumberKycAddressRequest.md) |  |  |

### Return type

[**ValidatePhoneNumberKycAddress200Response**](ValidatePhoneNumberKycAddress200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Address is deliverable, or the pre-check was skipped (no region supplied). |  -  |
| **400** | The country isn&#39;t offered, or the address could not be verified. When the provider returned usable corrections, &#x60;details.addressSuggestions&#x60; carries them per field for a one-click \&quot;apply suggestion\&quot; card. (Flat error envelope: &#x60;error&#x60; is the human message; &#x60;code&#x60;/&#x60;param&#x60;/&#x60;details&#x60; are top-level siblings.)  |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

