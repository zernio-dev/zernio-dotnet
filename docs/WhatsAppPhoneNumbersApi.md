# Zernio.Api.WhatsAppPhoneNumbersApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CheckWhatsAppNumberAvailability**](WhatsAppPhoneNumbersApi.md#checkwhatsappnumberavailability) | **GET** /v1/whatsapp/phone-numbers/availability | Check country availability |
| [**CreateWhatsAppNumberKycLink**](WhatsAppPhoneNumbersApi.md#createwhatsappnumberkyclink) | **POST** /v1/whatsapp/phone-numbers/kyc/share | Create a hosted KYC link |
| [**GetWhatsAppNumberInfo**](WhatsAppPhoneNumbersApi.md#getwhatsappnumberinfo) | **GET** /v1/whatsapp/number-info | Get number status |
| [**GetWhatsAppNumberKycForm**](WhatsAppPhoneNumbersApi.md#getwhatsappnumberkycform) | **GET** /v1/whatsapp/phone-numbers/kyc | Get KYC form spec |
| [**GetWhatsAppNumberRemediation**](WhatsAppPhoneNumbersApi.md#getwhatsappnumberremediation) | **GET** /v1/whatsapp/phone-numbers/{id}/remediate | Get declined requirements |
| [**GetWhatsAppPhoneNumber**](WhatsAppPhoneNumbersApi.md#getwhatsappphonenumber) | **GET** /v1/whatsapp/phone-numbers/{phoneNumberId} | Get phone number |
| [**GetWhatsAppPhoneNumbers**](WhatsAppPhoneNumbersApi.md#getwhatsappphonenumbers) | **GET** /v1/whatsapp/phone-numbers | List phone numbers |
| [**ListWhatsAppNumberCountries**](WhatsAppPhoneNumbersApi.md#listwhatsappnumbercountries) | **GET** /v1/whatsapp/phone-numbers/countries | List offerable number countries |
| [**PurchaseWhatsAppPhoneNumber**](WhatsAppPhoneNumbersApi.md#purchasewhatsappphonenumber) | **POST** /v1/whatsapp/phone-numbers/purchase | Purchase phone number |
| [**ReleaseWhatsAppPhoneNumber**](WhatsAppPhoneNumbersApi.md#releasewhatsappphonenumber) | **DELETE** /v1/whatsapp/phone-numbers/{phoneNumberId} | Release phone number |
| [**RemediateWhatsAppNumber**](WhatsAppPhoneNumbersApi.md#remediatewhatsappnumber) | **POST** /v1/whatsapp/phone-numbers/{id}/remediate | Resubmit a declined number |
| [**SearchAvailableWhatsAppNumbers**](WhatsAppPhoneNumbersApi.md#searchavailablewhatsappnumbers) | **GET** /v1/whatsapp/phone-numbers/available | Search available numbers |
| [**SubmitWhatsAppNumberKyc**](WhatsAppPhoneNumbersApi.md#submitwhatsappnumberkyc) | **POST** /v1/whatsapp/phone-numbers/kyc | Submit KYC |
| [**UploadWhatsAppNumberKycDocument**](WhatsAppPhoneNumbersApi.md#uploadwhatsappnumberkycdocument) | **POST** /v1/whatsapp/phone-numbers/kyc/upload-document | Upload a KYC document |
| [**ValidateWhatsAppNumberKycAddress**](WhatsAppPhoneNumbersApi.md#validatewhatsappnumberkycaddress) | **POST** /v1/whatsapp/phone-numbers/kyc/validate-address | Pre-validate KYC address |

<a id="checkwhatsappnumberavailability"></a>
# **CheckWhatsAppNumberAvailability**
> CheckPhoneNumberAvailability200Response CheckWhatsAppNumberAvailability (string country, string? numberType = null, bool? sms = null)

Check country availability

Deprecated alias of `/v1/phone-numbers/availability`; same contract. New integrations should use that path.  Pre-purchase check, so you can warn BEFORE a customer invests in KYC (regulated review is async, 1-3 days). Tells you whether we have deliverable inventory, and what address the customer needs:   - `addressConstraint: geo`  → the registered address MUST be in one of     the returned `areas` (the only place we have stock). A different-area     address passes pre-approval but the number can never be assigned.   - `addressConstraint: country` → any in-country address works.   - `addressConstraint: none` → field-only / instant country, no address. Call this before starting the KYC form for regulated countries. 

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
    public class CheckWhatsAppNumberAvailabilityExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var country = "country_example";  // string | ISO-2 country code.
            var numberType = "local";  // string? | Check a specific offered type (stock and address constraints are per type). Omitted = the country's default type. (optional) 
            var sms = true;  // bool? | Pass true when the buyer wants SMS: availability, areas, and areaOptions then describe the SMS-capable pool (an SMS purchase orders from it), not the wider voice-only pool. (optional) 

            try
            {
                // Check country availability
                CheckPhoneNumberAvailability200Response result = apiInstance.CheckWhatsAppNumberAvailability(country, numberType, sms);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.CheckWhatsAppNumberAvailability: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckWhatsAppNumberAvailabilityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check country availability
    ApiResponse<CheckPhoneNumberAvailability200Response> response = apiInstance.CheckWhatsAppNumberAvailabilityWithHttpInfo(country, numberType, sms);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.CheckWhatsAppNumberAvailabilityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **country** | **string** | ISO-2 country code. |  |
| **numberType** | **string?** | Check a specific offered type (stock and address constraints are per type). Omitted &#x3D; the country&#39;s default type. | [optional]  |
| **sms** | **bool?** | Pass true when the buyer wants SMS: availability, areas, and areaOptions then describe the SMS-capable pool (an SMS purchase orders from it), not the wider voice-only pool. | [optional]  |

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

<a id="createwhatsappnumberkyclink"></a>
# **CreateWhatsAppNumberKycLink**
> CreatePhoneNumberKycLink200Response CreateWhatsAppNumberKycLink (CreatePhoneNumberKycLinkRequest createPhoneNumberKycLinkRequest)

Create a hosted KYC link

Deprecated alias of `/v1/phone-numbers/kyc/share`; same contract. New integrations should use that path.  Create a single-use, 7-day hosted KYC link that your end customer completes WITHOUT a Zernio login — useful when the person who holds the ID and address is not your team. They fill the regulated verification on a Zernio-hosted page; the number provisions under YOUR account once they submit. Only regulated (KYC) countries are valid: a country that does not require KYC returns 400.  White-label the page with `branding` (your company name, logo, brand color). Supply `redirect_url` to send the end customer back to your own site after a successful submit (completion params are appended — see below). Listen for the `whatsapp.number.kyc_submitted` webhook to react when the form is completed. 

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
    public class CreateWhatsAppNumberKycLinkExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var createPhoneNumberKycLinkRequest = new CreatePhoneNumberKycLinkRequest(); // CreatePhoneNumberKycLinkRequest | 

            try
            {
                // Create a hosted KYC link
                CreatePhoneNumberKycLink200Response result = apiInstance.CreateWhatsAppNumberKycLink(createPhoneNumberKycLinkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.CreateWhatsAppNumberKycLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWhatsAppNumberKycLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a hosted KYC link
    ApiResponse<CreatePhoneNumberKycLink200Response> response = apiInstance.CreateWhatsAppNumberKycLinkWithHttpInfo(createPhoneNumberKycLinkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.CreateWhatsAppNumberKycLinkWithHttpInfo: " + e.Message);
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

<a id="getwhatsappnumberinfo"></a>
# **GetWhatsAppNumberInfo**
> GetWhatsAppNumberInfo200Response GetWhatsAppNumberInfo (string accountId)

Get number status

Live snapshot of a connected number straight from Meta: the phone-number node (display number, display name + approval, quality rating, messaging-limit tier, throughput, official-business badge, connection status, health_status) and its owning WhatsApp Business Account (name, business verification, timezone, health_status). Fetched live because Meta updates quality/tier/name/health over time; the call also refreshes the cached values shown on the connection card. 

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
    public class GetWhatsAppNumberInfoExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | WhatsApp social account ID

            try
            {
                // Get number status
                GetWhatsAppNumberInfo200Response result = apiInstance.GetWhatsAppNumberInfo(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppNumberInfo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppNumberInfoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get number status
    ApiResponse<GetWhatsAppNumberInfo200Response> response = apiInstance.GetWhatsAppNumberInfoWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppNumberInfoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | WhatsApp social account ID |  |

### Return type

[**GetWhatsAppNumberInfo200Response**](GetWhatsAppNumberInfo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Number + WABA status |  -  |
| **400** | Phone number ID not found on account |  -  |
| **401** | Unauthorized |  -  |
| **404** | WhatsApp account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getwhatsappnumberkycform"></a>
# **GetWhatsAppNumberKycForm**
> GetWhatsAppNumberKycForm200Response GetWhatsAppNumberKycForm (string country, string profileId)

Get KYC form spec

Deprecated alias of `/v1/phone-numbers/kyc`; same contract. New integrations should use that path.  For a Tier 3/4 country, the fields the end customer must provide (Telnyx regulatory requirements) before a number can be ordered: text, date, address, or file (document) per requirement. 

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
    public class GetWhatsAppNumberKycFormExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var country = "country_example";  // string | 
            var profileId = "profileId_example";  // string | 

            try
            {
                // Get KYC form spec
                GetWhatsAppNumberKycForm200Response result = apiInstance.GetWhatsAppNumberKycForm(country, profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppNumberKycForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppNumberKycFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get KYC form spec
    ApiResponse<GetWhatsAppNumberKycForm200Response> response = apiInstance.GetWhatsAppNumberKycFormWithHttpInfo(country, profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppNumberKycFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **country** | **string** |  |  |
| **profileId** | **string** |  |  |

### Return type

[**GetWhatsAppNumberKycForm200Response**](GetWhatsAppNumberKycForm200Response.md)

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

<a id="getwhatsappnumberremediation"></a>
# **GetWhatsAppNumberRemediation**
> GetWhatsAppNumberRemediation200Response GetWhatsAppNumberRemediation (string id)

Get declined requirements

Deprecated alias of `/v1/phone-numbers/{id}/remediate`; same contract. New integrations should use that path.  For a number in `regulatory_declined`, returns ONLY the requirements the reviewer flagged declined, as a form spec (same shape as the KYC form GET). The customer fixes just those — Telnyx supports correcting a declined requirement group and re-submitting it (no new number/group). Falls back to the full spec if the provider exposes no per-requirement flags. 

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
    public class GetWhatsAppNumberRemediationExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | WhatsAppPhoneNumber id.

            try
            {
                // Get declined requirements
                GetWhatsAppNumberRemediation200Response result = apiInstance.GetWhatsAppNumberRemediation(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppNumberRemediation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppNumberRemediationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get declined requirements
    ApiResponse<GetWhatsAppNumberRemediation200Response> response = apiInstance.GetWhatsAppNumberRemediationWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppNumberRemediationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | WhatsAppPhoneNumber id. |  |

### Return type

[**GetWhatsAppNumberRemediation200Response**](GetWhatsAppNumberRemediation200Response.md)

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

<a id="getwhatsappphonenumber"></a>
# **GetWhatsAppPhoneNumber**
> GetPhoneNumber200Response GetWhatsAppPhoneNumber (string phoneNumberId)

Get phone number

Deprecated alias of `/v1/phone-numbers/{id}`; same contract. New integrations should use that path.  Retrieve the current status of a purchased phone number. Poll this to track Meta pre-verification (US sync path) and, for regulated (Tier 3/4) numbers, the async lifecycle: pending_regulatory → active (or regulatory_declined). When a regulated number has an Onfido ID step, `onfidoVerificationUrl` appears here once the order is placed — forward it to the end user. (Or subscribe to the whatsapp.number.* webhooks instead of polling.) 

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
    public class GetWhatsAppPhoneNumberExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var phoneNumberId = "phoneNumberId_example";  // string | Phone number record ID

            try
            {
                // Get phone number
                GetPhoneNumber200Response result = apiInstance.GetWhatsAppPhoneNumber(phoneNumberId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get phone number
    ApiResponse<GetPhoneNumber200Response> response = apiInstance.GetWhatsAppPhoneNumberWithHttpInfo(phoneNumberId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberId** | **string** | Phone number record ID |  |

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

<a id="getwhatsappphonenumbers"></a>
# **GetWhatsAppPhoneNumbers**
> ListPhoneNumbers200Response GetWhatsAppPhoneNumbers (string? status = null, string? profileId = null)

List phone numbers

Deprecated alias of `/v1/phone-numbers`; same contract. New integrations should use that path.  List all WhatsApp phone numbers purchased by the authenticated user. By default, released numbers are excluded. Connected (bring-your-own) numbers are returned in the separate `connected` array — they are not billed and have no provisioning lifecycle. 

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
    public class GetWhatsAppPhoneNumbersExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var status = "provisioning";  // string? | Filter by status (by default excludes released numbers). NOTE: `status=pending_regulatory` returns the \"provisioning\" view — numbers still in review PLUS recently-declined (last 30 days) ones, so a failed registration surfaces (with `regulatoryDeclineReason`) instead of silently disappearing. Declined numbers can be re-submitted via POST /v1/whatsapp/phone-numbers/{id}/remediate. `verifying` is the short-lived state after the number is provisioned on our side while WhatsApp confirms the activation code; the number is not billed until it reaches `active`.  (optional) 
            var profileId = "profileId_example";  // string? | Filter by profile (optional) 

            try
            {
                // List phone numbers
                ListPhoneNumbers200Response result = apiInstance.GetWhatsAppPhoneNumbers(status, profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppPhoneNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWhatsAppPhoneNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List phone numbers
    ApiResponse<ListPhoneNumbers200Response> response = apiInstance.GetWhatsAppPhoneNumbersWithHttpInfo(status, profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.GetWhatsAppPhoneNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string?** | Filter by status (by default excludes released numbers). NOTE: &#x60;status&#x3D;pending_regulatory&#x60; returns the \&quot;provisioning\&quot; view — numbers still in review PLUS recently-declined (last 30 days) ones, so a failed registration surfaces (with &#x60;regulatoryDeclineReason&#x60;) instead of silently disappearing. Declined numbers can be re-submitted via POST /v1/whatsapp/phone-numbers/{id}/remediate. &#x60;verifying&#x60; is the short-lived state after the number is provisioned on our side while WhatsApp confirms the activation code; the number is not billed until it reaches &#x60;active&#x60;.  | [optional]  |
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
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listwhatsappnumbercountries"></a>
# **ListWhatsAppNumberCountries**
> ListWhatsAppNumberCountries200Response ListWhatsAppNumberCountries ()

List offerable number countries

Deprecated alias of `/v1/phone-numbers/countries`; same contract. New integrations should use that path.  The WhatsApp number countries available to purchase, each with its flat monthly price (cents), regulatory tier, whether it needs end-user KYC (Tier 3/4), and whether outbound calling is available (not BIC-blocked). Drives the country picker. Tier-4 countries appear only when enabled. 

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
    public class ListWhatsAppNumberCountriesExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);

            try
            {
                // List offerable number countries
                ListWhatsAppNumberCountries200Response result = apiInstance.ListWhatsAppNumberCountries();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.ListWhatsAppNumberCountries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWhatsAppNumberCountriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List offerable number countries
    ApiResponse<ListWhatsAppNumberCountries200Response> response = apiInstance.ListWhatsAppNumberCountriesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.ListWhatsAppNumberCountriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ListWhatsAppNumberCountries200Response**](ListWhatsAppNumberCountries200Response.md)

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

<a id="purchasewhatsappphonenumber"></a>
# **PurchaseWhatsAppPhoneNumber**
> PurchasePhoneNumber200Response PurchaseWhatsAppPhoneNumber (PurchaseWhatsAppPhoneNumberRequest purchaseWhatsAppPhoneNumberRequest)

Purchase phone number

Deprecated alias of `/v1/phone-numbers/purchase`; same contract. New integrations should use that path.  Payment-first: you do not pick a specific number, the system provisions one and auto-assigns it. With usage-based billing active and a payment method on file, the number provisions inline and bills per month on your usage-based invoice (there is no checkout redirect). No payment method on file returns `402 PAYMENT_REQUIRED`; a regulated country returns `202` with `status: \"kyc_required\"` and a `kycUrl`.  Requires usage-based billing (the Usage plan). The maximum number of phone numbers is determined by the user's plan. 

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
    public class PurchaseWhatsAppPhoneNumberExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var purchaseWhatsAppPhoneNumberRequest = new PurchaseWhatsAppPhoneNumberRequest(); // PurchaseWhatsAppPhoneNumberRequest | 

            try
            {
                // Purchase phone number
                PurchasePhoneNumber200Response result = apiInstance.PurchaseWhatsAppPhoneNumber(purchaseWhatsAppPhoneNumberRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.PurchaseWhatsAppPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PurchaseWhatsAppPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Purchase phone number
    ApiResponse<PurchasePhoneNumber200Response> response = apiInstance.PurchaseWhatsAppPhoneNumberWithHttpInfo(purchaseWhatsAppPhoneNumberRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.PurchaseWhatsAppPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **purchaseWhatsAppPhoneNumberRequest** | [**PurchaseWhatsAppPhoneNumberRequest**](PurchaseWhatsAppPhoneNumberRequest.md) |  |  |

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
| **409** | Either duplicate-purchase protection (code PURCHASE_VELOCITY: another number was purchased within the last 10 minutes; retry with allowMultiple: true to confirm), or the requested areaCode has no deliverable inventory right now (code AREA_CODE_UNAVAILABLE: pick another area or omit areaCode).  |  -  |
| **202** | Country requires end-user KYC before the number can be ordered. |  -  |
| **402** | Payment method required (Metronome user with no card on file). Response body carries code: PAYMENT_REQUIRED; add a card, then retry. |  -  |
| **422** | International numbers require usage-based billing (legacy Stripe users are US-only). Response body code: USAGE_BILLING_REQUIRED. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="releasewhatsappphonenumber"></a>
# **ReleaseWhatsAppPhoneNumber**
> ReleasePhoneNumber200Response ReleaseWhatsAppPhoneNumber (string phoneNumberId)

Release phone number

Deprecated alias of `/v1/phone-numbers/{id}`; same contract. New integrations should use that path.  Release a purchased phone number. This will: 1. Disconnect any linked WhatsApp social account 2. Decrement the Stripe subscription quantity (or cancel if last number) 3. Release the number from Telnyx 4. Mark the number as released 

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
    public class ReleaseWhatsAppPhoneNumberExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var phoneNumberId = "phoneNumberId_example";  // string | Phone number record ID

            try
            {
                // Release phone number
                ReleasePhoneNumber200Response result = apiInstance.ReleaseWhatsAppPhoneNumber(phoneNumberId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.ReleaseWhatsAppPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReleaseWhatsAppPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Release phone number
    ApiResponse<ReleasePhoneNumber200Response> response = apiInstance.ReleaseWhatsAppPhoneNumberWithHttpInfo(phoneNumberId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.ReleaseWhatsAppPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberId** | **string** | Phone number record ID |  |

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

<a id="remediatewhatsappnumber"></a>
# **RemediateWhatsAppNumber**
> RemediatePhoneNumber200Response RemediateWhatsAppNumber (string id, RemediatePhoneNumberRequest remediatePhoneNumberRequest)

Resubmit a declined number

Deprecated alias of `/v1/phone-numbers/{id}/remediate`; same contract. New integrations should use that path.  Submit corrected values/documents for the declined requirement(s). We PATCH them onto the SAME requirement group and re-submit it for approval; the number goes `regulatory_declined` → `pending_regulatory`. No new number and no new billing. Body shape matches the KYC submit (values / documents / address) — send only the corrected fields. 

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
    public class RemediateWhatsAppNumberExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var remediatePhoneNumberRequest = new RemediatePhoneNumberRequest(); // RemediatePhoneNumberRequest | 

            try
            {
                // Resubmit a declined number
                RemediatePhoneNumber200Response result = apiInstance.RemediateWhatsAppNumber(id, remediatePhoneNumberRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.RemediateWhatsAppNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemediateWhatsAppNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resubmit a declined number
    ApiResponse<RemediatePhoneNumber200Response> response = apiInstance.RemediateWhatsAppNumberWithHttpInfo(id, remediatePhoneNumberRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.RemediateWhatsAppNumberWithHttpInfo: " + e.Message);
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

<a id="searchavailablewhatsappnumbers"></a>
# **SearchAvailableWhatsAppNumbers**
> SearchAvailableWhatsAppNumbers200Response SearchAvailableWhatsAppNumbers (string? country = null, string? type = null, string? prefix = null, string? locality = null, string? contains = null, int? limit = null)

Search available numbers

Deprecated alias of `/v1/phone-numbers/available`; same contract. New integrations should use that path.  Search the provider's inventory for numbers available to purchase in a country (default US). Optional filters narrow the results. The country must be offerable (see GET /v1/whatsapp/phone-numbers/countries). 

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
    public class SearchAvailableWhatsAppNumbersExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var country = "\"US\"";  // string? |  (optional)  (default to "US")
            var type = "type_example";  // string? | Number type; defaults to the country's WhatsApp-safe type (optional) 
            var prefix = "prefix_example";  // string? | Area code (optional) 
            var locality = "locality_example";  // string? | City (optional) 
            var contains = "contains_example";  // string? | Pattern to match within the number (optional) 
            var limit = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // Search available numbers
                SearchAvailableWhatsAppNumbers200Response result = apiInstance.SearchAvailableWhatsAppNumbers(country, type, prefix, locality, contains, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.SearchAvailableWhatsAppNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchAvailableWhatsAppNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search available numbers
    ApiResponse<SearchAvailableWhatsAppNumbers200Response> response = apiInstance.SearchAvailableWhatsAppNumbersWithHttpInfo(country, type, prefix, locality, contains, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.SearchAvailableWhatsAppNumbersWithHttpInfo: " + e.Message);
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
| **limit** | **int?** |  | [optional] [default to 20] |

### Return type

[**SearchAvailableWhatsAppNumbers200Response**](SearchAvailableWhatsAppNumbers200Response.md)

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

<a id="submitwhatsappnumberkyc"></a>
# **SubmitWhatsAppNumberKyc**
> SubmitPhoneNumberKyc200Response SubmitWhatsAppNumberKyc (SubmitWhatsAppNumberKycRequest submitWhatsAppNumberKycRequest)

Submit KYC

Deprecated alias of `/v1/phone-numbers/kyc`; same contract. New integrations should use that path.  Submit the end customer's KYC (textual values, uploaded documents, address) for a Tier 3/4 country. Documents are streamed straight to the number provider and are not stored by Zernio. Builds + submits a regulatory requirement group and claims a pending_regulatory slot; the number is ordered + activated once the provider approves (asynchronous). A customer may hold several same-country numbers in review at once; a double-submit of the SAME attempt is deduped via `submissionId`.  For an ID-card document requirement, carriers commonly require BOTH sides: combine the front and back into a single file before uploading (the dashboard does this automatically). A one-sided ID is a common decline reason; fix it via POST /v1/whatsapp/phone-numbers/{id}/remediate.  Before submitting, call GET /v1/whatsapp/phone-numbers/availability to check the country has deliverable inventory and, for geographic-match countries, which area the address must be in — otherwise the submission can pass review yet never be assignable a number. 

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
    public class SubmitWhatsAppNumberKycExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var submitWhatsAppNumberKycRequest = new SubmitWhatsAppNumberKycRequest(); // SubmitWhatsAppNumberKycRequest | 

            try
            {
                // Submit KYC
                SubmitPhoneNumberKyc200Response result = apiInstance.SubmitWhatsAppNumberKyc(submitWhatsAppNumberKycRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.SubmitWhatsAppNumberKyc: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubmitWhatsAppNumberKycWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit KYC
    ApiResponse<SubmitPhoneNumberKyc200Response> response = apiInstance.SubmitWhatsAppNumberKycWithHttpInfo(submitWhatsAppNumberKycRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.SubmitWhatsAppNumberKycWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **submitWhatsAppNumberKycRequest** | [**SubmitWhatsAppNumberKycRequest**](SubmitWhatsAppNumberKycRequest.md) |  |  |

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
| **409** | Either reuse was requested but no prior approved verification exists for this country, or the requested areaCode has no deliverable inventory right now (code: area_code_unavailable; pick another area and resubmit). |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadwhatsappnumberkycdocument"></a>
# **UploadWhatsAppNumberKycDocument**
> UploadPhoneNumberKycDocument200Response UploadWhatsAppNumberKycDocument (string xFilename, FileParameter body)

Upload a KYC document

Deprecated alias of `/v1/phone-numbers/kyc/upload-document`; same contract. New integrations should use that path.  Upload ONE document and get back its provider document id, to reference from POST /v1/whatsapp/phone-numbers/kyc via `documents[].documentId`. Send the RAW file bytes as the request body (not base64); put the filename in the `X-Filename` header. Uploading documents one-per-request keeps each request under the ~4.5MB body limit. The document streams straight to the number provider and is not stored by Zernio. 

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
    public class UploadWhatsAppNumberKycDocumentExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var xFilename = "xFilename_example";  // string | URL-encoded original filename.
            var body = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // FileParameter | 

            try
            {
                // Upload a KYC document
                UploadPhoneNumberKycDocument200Response result = apiInstance.UploadWhatsAppNumberKycDocument(xFilename, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.UploadWhatsAppNumberKycDocument: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadWhatsAppNumberKycDocumentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload a KYC document
    ApiResponse<UploadPhoneNumberKycDocument200Response> response = apiInstance.UploadWhatsAppNumberKycDocumentWithHttpInfo(xFilename, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.UploadWhatsAppNumberKycDocumentWithHttpInfo: " + e.Message);
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

<a id="validatewhatsappnumberkycaddress"></a>
# **ValidateWhatsAppNumberKycAddress**
> ValidatePhoneNumberKycAddress200Response ValidateWhatsAppNumberKycAddress (ValidatePhoneNumberKycAddressRequest validatePhoneNumberKycAddressRequest)

Pre-validate KYC address

Deprecated alias of `/v1/phone-numbers/kyc/validate-address`; same contract. New integrations should use that path.  Optional early check for the address step of a Tier 4 (end-user identity) registration: validates a postal address for deliverability BEFORE the full KYC submit, so it can be corrected before any documents are uploaded. The full submit (POST /v1/whatsapp/phone-numbers/kyc) re-validates the address, so this call is purely a fast feedback path and skipping it is safe. Only the postal address is sent (no documents, no gov-ID fields). A region (`administrative_area`) is required by the validator; when it is omitted the pre-check is skipped and `{ ok: true, skipped: true }` is returned (the final submit still validates). 

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
    public class ValidateWhatsAppNumberKycAddressExample
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
            var apiInstance = new WhatsAppPhoneNumbersApi(httpClient, config, httpClientHandler);
            var validatePhoneNumberKycAddressRequest = new ValidatePhoneNumberKycAddressRequest(); // ValidatePhoneNumberKycAddressRequest | 

            try
            {
                // Pre-validate KYC address
                ValidatePhoneNumberKycAddress200Response result = apiInstance.ValidateWhatsAppNumberKycAddress(validatePhoneNumberKycAddressRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.ValidateWhatsAppNumberKycAddress: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ValidateWhatsAppNumberKycAddressWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pre-validate KYC address
    ApiResponse<ValidatePhoneNumberKycAddress200Response> response = apiInstance.ValidateWhatsAppNumberKycAddressWithHttpInfo(validatePhoneNumberKycAddressRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WhatsAppPhoneNumbersApi.ValidateWhatsAppNumberKycAddressWithHttpInfo: " + e.Message);
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

