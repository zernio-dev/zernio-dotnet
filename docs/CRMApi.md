# Zernio.Api.CRMApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCrmActivity**](CRMApi.md#createcrmactivity) | **POST** /v1/crm/{accountId}/contacts/{contactId}/activities | Log a CRM activity |
| [**CreateCrmContact**](CRMApi.md#createcrmcontact) | **POST** /v1/crm/{accountId}/contacts | Create a CRM contact |
| [**GetCrmContact**](CRMApi.md#getcrmcontact) | **GET** /v1/crm/{accountId}/contacts/{contactId} | Get a CRM contact |
| [**GetCrmDeal**](CRMApi.md#getcrmdeal) | **GET** /v1/crm/{accountId}/deals/{dealId} | Get a CRM deal |
| [**ListCrmDeals**](CRMApi.md#listcrmdeals) | **GET** /v1/crm/{accountId}/deals | List CRM deals |
| [**ListCrmOwners**](CRMApi.md#listcrmowners) | **GET** /v1/crm/{accountId}/owners | List CRM owners |
| [**SearchCrmContacts**](CRMApi.md#searchcrmcontacts) | **GET** /v1/crm/{accountId}/contacts/search | Search CRM contacts |
| [**UpdateCrmContact**](CRMApi.md#updatecrmcontact) | **PATCH** /v1/crm/{accountId}/contacts/{contactId} | Update a CRM contact |
| [**UpdateCrmDeal**](CRMApi.md#updatecrmdeal) | **PATCH** /v1/crm/{accountId}/deals/{dealId} | Update a CRM deal |

<a id="createcrmactivity"></a>
# **CreateCrmActivity**
> CreateCrmActivity201Response CreateCrmActivity (string accountId, string contactId, CreateCrmActivityRequest createCrmActivityRequest)

Log a CRM activity

Log something that happened with a person on their CRM record.  - HubSpot: a Communication on the contact's timeline for `channel` `whatsapp` or `sms`, otherwise a Note. The subject and direction lead the text. - Salesforce: a completed Task on the Contact or Lead (`WhoId`), dated `occurredAt`, with `body` as its comments. `channel: call` logs a call. - HighLevel: a plain-text note on the contact. HighLevel dates a note when it is logged, so the subject (or channel), direction and `occurredAt` lead its text.  To log inbox conversations automatically instead, turn on `logMessages` in the CRM settings.

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
    public class CreateCrmActivityExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var contactId = "contactId_example";  // string | The CRM's own id. HubSpot contact id, Salesforce Contact (`003...`) or Lead (`00Q...`) id, or HighLevel contact id.
            var createCrmActivityRequest = new CreateCrmActivityRequest(); // CreateCrmActivityRequest | 

            try
            {
                // Log a CRM activity
                CreateCrmActivity201Response result = apiInstance.CreateCrmActivity(accountId, contactId, createCrmActivityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.CreateCrmActivity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCrmActivityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Log a CRM activity
    ApiResponse<CreateCrmActivity201Response> response = apiInstance.CreateCrmActivityWithHttpInfo(accountId, contactId, createCrmActivityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.CreateCrmActivityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **contactId** | **string** | The CRM&#39;s own id. HubSpot contact id, Salesforce Contact (&#x60;003...&#x60;) or Lead (&#x60;00Q...&#x60;) id, or HighLevel contact id. |  |
| **createCrmActivityRequest** | [**CreateCrmActivityRequest**](CreateCrmActivityRequest.md) |  |  |

### Return type

[**CreateCrmActivity201Response**](CreateCrmActivity201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The logged activity. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | The account exists but is disconnected (deactivated, or flagged as needing reconnection). Code &#x60;account_disconnected&#x60;.  &#x60;details&#x60; names the account (&#x60;accountId&#x60;, &#x60;platform&#x60;, &#x60;username&#x60;) with its &#x60;disconnectReason&#x60;, &#x60;disconnectionType&#x60;, &#x60;unhealthySince&#x60; and &#x60;action: reconnect&#x60;.  Reconnect the account (its accountId stays the same), then retry. The disconnect is also sent as the &#x60;account.disconnected&#x60; webhook. |  -  |
| **422** | The CRM refused the values: a validation rule, a required field, a bad picklist value or an unknown field. Code &#x60;crm_validation_failed&#x60;; &#x60;details.errors&#x60; lists the CRM&#39;s own errors, each with &#x60;code&#x60;, &#x60;message&#x60; and the &#x60;fields&#x60; at fault when the CRM names them. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcrmcontact"></a>
# **CreateCrmContact**
> CreateCrmContact201Response CreateCrmContact (string accountId, CreateCrmContactRequest createCrmContactRequest)

Create a CRM contact

Create a person in the connected CRM. HubSpot creates a contact. Salesforce creates a Lead or a Contact: `createAs`, else the connection's `createAs` setting (default `lead`).  Salesforce requires `lastName` on both, and `company` on a Lead (`[not provided]` when you send none). A Contact takes its company from its Account: set `properties.AccountId` instead.  HighLevel creates a contact in the connected location. A location that does not allow duplicates answers 409 with the existing contact.  Anything the CRM refuses (a required field, a validation rule, a duplicate rule) comes back as 422 or 409 with the CRM's own errors in `details.errors`.

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
    public class CreateCrmContactExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var createCrmContactRequest = new CreateCrmContactRequest(); // CreateCrmContactRequest | 

            try
            {
                // Create a CRM contact
                CreateCrmContact201Response result = apiInstance.CreateCrmContact(accountId, createCrmContactRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.CreateCrmContact: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCrmContactWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a CRM contact
    ApiResponse<CreateCrmContact201Response> response = apiInstance.CreateCrmContactWithHttpInfo(accountId, createCrmContactRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.CreateCrmContactWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **createCrmContactRequest** | [**CreateCrmContactRequest**](CreateCrmContactRequest.md) |  |  |

### Return type

[**CreateCrmContact201Response**](CreateCrmContact201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The created contact, read back from the CRM. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | &#x60;crm_duplicate_record&#x60;: the CRM refused a duplicate (HubSpot: the email belongs to another contact; Salesforce: a duplicate rule; HighLevel: a location that does not allow duplicate contacts). &#x60;details.existingId&#x60; is the existing record when the CRM names it.  &#x60;account_disconnected&#x60;: the CRM account needs reconnecting; see AccountDisconnected. |  -  |
| **422** | The CRM refused the values: a validation rule, a required field, a bad picklist value or an unknown field. Code &#x60;crm_validation_failed&#x60;; &#x60;details.errors&#x60; lists the CRM&#39;s own errors, each with &#x60;code&#x60;, &#x60;message&#x60; and the &#x60;fields&#x60; at fault when the CRM names them. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcrmcontact"></a>
# **GetCrmContact**
> CreateCrmContact201Response GetCrmContact (string accountId, string contactId, string? properties = null, bool? includeRaw = null)

Get a CRM contact

Read one person from the connected CRM. On Salesforce the id can be a Contact (`003...`) or a Lead (`00Q...`).

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
    public class GetCrmContactExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var contactId = "contactId_example";  // string | The CRM's own id. HubSpot contact id, Salesforce Contact (`003...`) or Lead (`00Q...`) id, or HighLevel contact id.
            var properties = "properties_example";  // string? | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. On HighLevel, a field of the record (`source`, `status`), or a custom field by id or key. (optional) 
            var includeRaw = false;  // bool? | Also return the CRM's own record as `raw`. (optional)  (default to false)

            try
            {
                // Get a CRM contact
                CreateCrmContact201Response result = apiInstance.GetCrmContact(accountId, contactId, properties, includeRaw);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.GetCrmContact: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCrmContactWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a CRM contact
    ApiResponse<CreateCrmContact201Response> response = apiInstance.GetCrmContactWithHttpInfo(accountId, contactId, properties, includeRaw);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.GetCrmContactWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **contactId** | **string** | The CRM&#39;s own id. HubSpot contact id, Salesforce Contact (&#x60;003...&#x60;) or Lead (&#x60;00Q...&#x60;) id, or HighLevel contact id. |  |
| **properties** | **string?** | Comma-separated native field names to return in &#x60;properties&#x60; (at most 50), for example &#x60;lifecyclestage,hs_lead_status&#x60; or &#x60;LeadSource,Industry__c&#x60;. On HighLevel, a field of the record (&#x60;source&#x60;, &#x60;status&#x60;), or a custom field by id or key. | [optional]  |
| **includeRaw** | **bool?** | Also return the CRM&#39;s own record as &#x60;raw&#x60;. | [optional] [default to false] |

### Return type

[**CreateCrmContact201Response**](CreateCrmContact201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The contact. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | The account exists but is disconnected (deactivated, or flagged as needing reconnection). Code &#x60;account_disconnected&#x60;.  &#x60;details&#x60; names the account (&#x60;accountId&#x60;, &#x60;platform&#x60;, &#x60;username&#x60;) with its &#x60;disconnectReason&#x60;, &#x60;disconnectionType&#x60;, &#x60;unhealthySince&#x60; and &#x60;action: reconnect&#x60;.  Reconnect the account (its accountId stays the same), then retry. The disconnect is also sent as the &#x60;account.disconnected&#x60; webhook. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcrmdeal"></a>
# **GetCrmDeal**
> GetCrmDeal200Response GetCrmDeal (string accountId, string dealId, string? properties = null, bool? includeRaw = null)

Get a CRM deal

Read one deal (HubSpot), Opportunity (Salesforce) or opportunity (HighLevel) with its contacts.

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
    public class GetCrmDealExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var dealId = "dealId_example";  // string | HubSpot deal id, Salesforce Opportunity id (`006...`) or HighLevel opportunity id.
            var properties = "properties_example";  // string? | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. On HighLevel, a field of the record (`source`, `status`), or a custom field by id or key. (optional) 
            var includeRaw = false;  // bool? | Also return the CRM's own record as `raw`. (optional)  (default to false)

            try
            {
                // Get a CRM deal
                GetCrmDeal200Response result = apiInstance.GetCrmDeal(accountId, dealId, properties, includeRaw);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.GetCrmDeal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCrmDealWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a CRM deal
    ApiResponse<GetCrmDeal200Response> response = apiInstance.GetCrmDealWithHttpInfo(accountId, dealId, properties, includeRaw);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.GetCrmDealWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **dealId** | **string** | HubSpot deal id, Salesforce Opportunity id (&#x60;006...&#x60;) or HighLevel opportunity id. |  |
| **properties** | **string?** | Comma-separated native field names to return in &#x60;properties&#x60; (at most 50), for example &#x60;lifecyclestage,hs_lead_status&#x60; or &#x60;LeadSource,Industry__c&#x60;. On HighLevel, a field of the record (&#x60;source&#x60;, &#x60;status&#x60;), or a custom field by id or key. | [optional]  |
| **includeRaw** | **bool?** | Also return the CRM&#39;s own record as &#x60;raw&#x60;. | [optional] [default to false] |

### Return type

[**GetCrmDeal200Response**](GetCrmDeal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The deal. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | The account exists but is disconnected (deactivated, or flagged as needing reconnection). Code &#x60;account_disconnected&#x60;.  &#x60;details&#x60; names the account (&#x60;accountId&#x60;, &#x60;platform&#x60;, &#x60;username&#x60;) with its &#x60;disconnectReason&#x60;, &#x60;disconnectionType&#x60;, &#x60;unhealthySince&#x60; and &#x60;action: reconnect&#x60;.  Reconnect the account (its accountId stays the same), then retry. The disconnect is also sent as the &#x60;account.disconnected&#x60; webhook. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcrmdeals"></a>
# **ListCrmDeals**
> ListCrmDeals200Response ListCrmDeals (string accountId, string? stage = null, DateTime? updatedSince = null, string? properties = null, bool? includeRaw = null, int? limit = null, string? cursor = null)

List CRM deals

List deals (HubSpot) or Opportunities (Salesforce), most recently changed first, or a HighLevel location's opportunities in HighLevel's own order.  HubSpot needs the portal to have granted `crm.objects.deals.read`; otherwise 403 `crm_scope_missing`. HighLevel cannot filter by update time: `updatedSince` answers 400 there.

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
    public class ListCrmDealsExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var stage = "stage_example";  // string? | Only deals in this stage. HubSpot takes the stage's internal id (`closedwon`, `appointmentscheduled`); Salesforce the `StageName` (`Closed Won`); HighLevel the pipeline stage id. (optional) 
            var updatedSince = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Only deals changed at or after this time. HubSpot and Salesforce only. (optional) 
            var properties = "properties_example";  // string? | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. On HighLevel, a field of the record (`source`, `status`), or a custom field by id or key. (optional) 
            var includeRaw = false;  // bool? | Also return the CRM's own record as `raw`. (optional)  (default to false)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? | The `nextCursor` of the previous page, unchanged. (optional) 

            try
            {
                // List CRM deals
                ListCrmDeals200Response result = apiInstance.ListCrmDeals(accountId, stage, updatedSince, properties, includeRaw, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.ListCrmDeals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCrmDealsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List CRM deals
    ApiResponse<ListCrmDeals200Response> response = apiInstance.ListCrmDealsWithHttpInfo(accountId, stage, updatedSince, properties, includeRaw, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.ListCrmDealsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **stage** | **string?** | Only deals in this stage. HubSpot takes the stage&#39;s internal id (&#x60;closedwon&#x60;, &#x60;appointmentscheduled&#x60;); Salesforce the &#x60;StageName&#x60; (&#x60;Closed Won&#x60;); HighLevel the pipeline stage id. | [optional]  |
| **updatedSince** | **DateTime?** | Only deals changed at or after this time. HubSpot and Salesforce only. | [optional]  |
| **properties** | **string?** | Comma-separated native field names to return in &#x60;properties&#x60; (at most 50), for example &#x60;lifecyclestage,hs_lead_status&#x60; or &#x60;LeadSource,Industry__c&#x60;. On HighLevel, a field of the record (&#x60;source&#x60;, &#x60;status&#x60;), or a custom field by id or key. | [optional]  |
| **includeRaw** | **bool?** | Also return the CRM&#39;s own record as &#x60;raw&#x60;. | [optional] [default to false] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** | The &#x60;nextCursor&#x60; of the previous page, unchanged. | [optional]  |

### Return type

[**ListCrmDeals200Response**](ListCrmDeals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One page of deals. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | The account exists but is disconnected (deactivated, or flagged as needing reconnection). Code &#x60;account_disconnected&#x60;.  &#x60;details&#x60; names the account (&#x60;accountId&#x60;, &#x60;platform&#x60;, &#x60;username&#x60;) with its &#x60;disconnectReason&#x60;, &#x60;disconnectionType&#x60;, &#x60;unhealthySince&#x60; and &#x60;action: reconnect&#x60;.  Reconnect the account (its accountId stays the same), then retry. The disconnect is also sent as the &#x60;account.disconnected&#x60; webhook. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcrmowners"></a>
# **ListCrmOwners**
> ListCrmOwners200Response ListCrmOwners (string accountId, bool? includeRaw = null, int? limit = null, string? cursor = null)

List CRM owners

List the users records can be assigned to: HubSpot owners, active standard Salesforce users, or the HighLevel location's users. Use an `id` as `ownerId` on contacts and deals.  HubSpot needs `crm.objects.owners.read`, an optional scope portals approve when they connect; without it, 403 `crm_scope_missing` asks to reconnect HubSpot. HighLevel needs `users.readonly`: a location installed before Zernio asked for it answers 403 `crm_scope_missing` until it reconnects.

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
    public class ListCrmOwnersExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var includeRaw = false;  // bool? | Also return the CRM's own record as `raw`. (optional)  (default to false)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? | The `nextCursor` of the previous page, unchanged. (optional) 

            try
            {
                // List CRM owners
                ListCrmOwners200Response result = apiInstance.ListCrmOwners(accountId, includeRaw, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.ListCrmOwners: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCrmOwnersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List CRM owners
    ApiResponse<ListCrmOwners200Response> response = apiInstance.ListCrmOwnersWithHttpInfo(accountId, includeRaw, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.ListCrmOwnersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **includeRaw** | **bool?** | Also return the CRM&#39;s own record as &#x60;raw&#x60;. | [optional] [default to false] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** | The &#x60;nextCursor&#x60; of the previous page, unchanged. | [optional]  |

### Return type

[**ListCrmOwners200Response**](ListCrmOwners200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One page of owners. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | The account exists but is disconnected (deactivated, or flagged as needing reconnection). Code &#x60;account_disconnected&#x60;.  &#x60;details&#x60; names the account (&#x60;accountId&#x60;, &#x60;platform&#x60;, &#x60;username&#x60;) with its &#x60;disconnectReason&#x60;, &#x60;disconnectionType&#x60;, &#x60;unhealthySince&#x60; and &#x60;action: reconnect&#x60;.  Reconnect the account (its accountId stays the same), then retry. The disconnect is also sent as the &#x60;account.disconnected&#x60; webhook. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="searchcrmcontacts"></a>
# **SearchCrmContacts**
> SearchCrmContacts200Response SearchCrmContacts (string accountId, string? q = null, string? email = null, string? phone = null, string? properties = null, bool? includeRaw = null, int? limit = null, string? cursor = null)

Search CRM contacts

Find people in the connected CRM by free text, email or phone. Send exactly one of `q`, `email` or `phone`.  HubSpot searches contacts. Salesforce searches Contacts and Leads that are not converted (`objectType` tells which), newest change first. HighLevel searches the location's contacts.  - `email` is an exact match. - `phone` takes an international number and matches it however the CRM stored it (\"+44 7911 123456\", \"07911 123456\"). - `q` searches names, emails, phones and company. On Salesforce, `q` and `phone` use the search index, so a record saved in the last few minutes may not show yet; `email` never lags. - On HighLevel, `email` and `phone` use the location's duplicate check: at most one contact, with no next page.

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
    public class SearchCrmContactsExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var q = "q_example";  // string? | Free text, at least 2 characters. (optional) 
            var email = "email_example";  // string? |  (optional) 
            var phone = "phone_example";  // string? | International number with its country code, for example `+14155550100`. (optional) 
            var properties = "properties_example";  // string? | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. On HighLevel, a field of the record (`source`, `status`), or a custom field by id or key. (optional) 
            var includeRaw = false;  // bool? | Also return the CRM's own record as `raw`. (optional)  (default to false)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? | The `nextCursor` of the previous page, unchanged. (optional) 

            try
            {
                // Search CRM contacts
                SearchCrmContacts200Response result = apiInstance.SearchCrmContacts(accountId, q, email, phone, properties, includeRaw, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.SearchCrmContacts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchCrmContactsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search CRM contacts
    ApiResponse<SearchCrmContacts200Response> response = apiInstance.SearchCrmContactsWithHttpInfo(accountId, q, email, phone, properties, includeRaw, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.SearchCrmContactsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **q** | **string?** | Free text, at least 2 characters. | [optional]  |
| **email** | **string?** |  | [optional]  |
| **phone** | **string?** | International number with its country code, for example &#x60;+14155550100&#x60;. | [optional]  |
| **properties** | **string?** | Comma-separated native field names to return in &#x60;properties&#x60; (at most 50), for example &#x60;lifecyclestage,hs_lead_status&#x60; or &#x60;LeadSource,Industry__c&#x60;. On HighLevel, a field of the record (&#x60;source&#x60;, &#x60;status&#x60;), or a custom field by id or key. | [optional]  |
| **includeRaw** | **bool?** | Also return the CRM&#39;s own record as &#x60;raw&#x60;. | [optional] [default to false] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** | The &#x60;nextCursor&#x60; of the previous page, unchanged. | [optional]  |

### Return type

[**SearchCrmContacts200Response**](SearchCrmContacts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Matching contacts, one page. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | The account exists but is disconnected (deactivated, or flagged as needing reconnection). Code &#x60;account_disconnected&#x60;.  &#x60;details&#x60; names the account (&#x60;accountId&#x60;, &#x60;platform&#x60;, &#x60;username&#x60;) with its &#x60;disconnectReason&#x60;, &#x60;disconnectionType&#x60;, &#x60;unhealthySince&#x60; and &#x60;action: reconnect&#x60;.  Reconnect the account (its accountId stays the same), then retry. The disconnect is also sent as the &#x60;account.disconnected&#x60; webhook. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecrmcontact"></a>
# **UpdateCrmContact**
> CreateCrmContact201Response UpdateCrmContact (string accountId, string contactId, CrmContactInput crmContactInput)

Update a CRM contact

Change fields on a person in the connected CRM. Send only what changes; `null` clears a field. Native fields go in `properties`.  On Salesforce, `company` applies to Leads only (400 on a Contact).

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
    public class UpdateCrmContactExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var contactId = "contactId_example";  // string | The CRM's own id. HubSpot contact id, Salesforce Contact (`003...`) or Lead (`00Q...`) id, or HighLevel contact id.
            var crmContactInput = new CrmContactInput(); // CrmContactInput | 

            try
            {
                // Update a CRM contact
                CreateCrmContact201Response result = apiInstance.UpdateCrmContact(accountId, contactId, crmContactInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.UpdateCrmContact: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCrmContactWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a CRM contact
    ApiResponse<CreateCrmContact201Response> response = apiInstance.UpdateCrmContactWithHttpInfo(accountId, contactId, crmContactInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.UpdateCrmContactWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **contactId** | **string** | The CRM&#39;s own id. HubSpot contact id, Salesforce Contact (&#x60;003...&#x60;) or Lead (&#x60;00Q...&#x60;) id, or HighLevel contact id. |  |
| **crmContactInput** | [**CrmContactInput**](CrmContactInput.md) |  |  |

### Return type

[**CreateCrmContact201Response**](CreateCrmContact201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated contact, read back from the CRM. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | &#x60;crm_duplicate_record&#x60;: the CRM refused a duplicate (HubSpot: the email belongs to another contact; Salesforce: a duplicate rule; HighLevel: a location that does not allow duplicate contacts). &#x60;details.existingId&#x60; is the existing record when the CRM names it.  &#x60;account_disconnected&#x60;: the CRM account needs reconnecting; see AccountDisconnected. |  -  |
| **422** | The CRM refused the values: a validation rule, a required field, a bad picklist value or an unknown field. Code &#x60;crm_validation_failed&#x60;; &#x60;details.errors&#x60; lists the CRM&#39;s own errors, each with &#x60;code&#x60;, &#x60;message&#x60; and the &#x60;fields&#x60; at fault when the CRM names them. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecrmdeal"></a>
# **UpdateCrmDeal**
> GetCrmDeal200Response UpdateCrmDeal (string accountId, string dealId, UpdateCrmDealRequest updateCrmDealRequest)

Update a CRM deal

Move a deal to another stage, or change its amount, close date, owner or native fields. Send only what changes.  HubSpot needs `crm.objects.deals.write`, an optional scope portals approve when they connect; without it, 403 `crm_scope_missing` asks to reconnect HubSpot. `currency` only works on multi-currency HubSpot portals and Salesforce orgs.  HighLevel: `stage` is the pipeline stage id, `amount` the opportunity value, and `properties.status` (`open`, `won`, `lost`, `abandoned`) marks it won or lost. Its opportunities have no close date or currency of their own: `closeDate` and `currency` answer 400.  Updating needs `opportunities.write`, which the Zernio HighLevel app does not request yet, so this call answers 403 `crm_scope_missing` on HighLevel for now.

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
    public class UpdateCrmDealExample
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
            var apiInstance = new CRMApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | The connected HubSpot, Salesforce or HighLevel account (`GET /v1/accounts?platform=hubspot`, `salesforce` or `gohighlevel`).
            var dealId = "dealId_example";  // string | HubSpot deal id, Salesforce Opportunity id (`006...`) or HighLevel opportunity id.
            var updateCrmDealRequest = new UpdateCrmDealRequest(); // UpdateCrmDealRequest | 

            try
            {
                // Update a CRM deal
                GetCrmDeal200Response result = apiInstance.UpdateCrmDeal(accountId, dealId, updateCrmDealRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CRMApi.UpdateCrmDeal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCrmDealWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a CRM deal
    ApiResponse<GetCrmDeal200Response> response = apiInstance.UpdateCrmDealWithHttpInfo(accountId, dealId, updateCrmDealRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CRMApi.UpdateCrmDealWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | The connected HubSpot, Salesforce or HighLevel account (&#x60;GET /v1/accounts?platform&#x3D;hubspot&#x60;, &#x60;salesforce&#x60; or &#x60;gohighlevel&#x60;). |  |
| **dealId** | **string** | HubSpot deal id, Salesforce Opportunity id (&#x60;006...&#x60;) or HighLevel opportunity id. |  |
| **updateCrmDealRequest** | [**UpdateCrmDealRequest**](UpdateCrmDealRequest.md) |  |  |

### Return type

[**GetCrmDeal200Response**](GetCrmDeal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated deal, read back from the CRM. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | &#x60;crm_scope_missing&#x60;: the connection did not grant a scope this call needs (&#x60;details.scope&#x60;), typically a HubSpot optional scope added after the portal connected, or a HighLevel scope (such as &#x60;users.readonly&#x60;) added after the location installed the app. Reconnect the CRM and approve it; the account id stays the same.  &#x60;crm_access_denied&#x60;: the CRM refused the connected user (Salesforce field-level security or sharing, a HubSpot permission). &#x60;details.errors&#x60; holds the CRM&#39;s own errors. |  -  |
| **404** | &#x60;account_not_found&#x60;: the accountId is not a CRM account you can access. &#x60;crm_record_not_found&#x60;: the CRM has no record with this id (deleted, merged, or another object type). |  -  |
| **409** | The account exists but is disconnected (deactivated, or flagged as needing reconnection). Code &#x60;account_disconnected&#x60;.  &#x60;details&#x60; names the account (&#x60;accountId&#x60;, &#x60;platform&#x60;, &#x60;username&#x60;) with its &#x60;disconnectReason&#x60;, &#x60;disconnectionType&#x60;, &#x60;unhealthySince&#x60; and &#x60;action: reconnect&#x60;.  Reconnect the account (its accountId stays the same), then retry. The disconnect is also sent as the &#x60;account.disconnected&#x60; webhook. |  -  |
| **422** | The CRM refused the values: a validation rule, a required field, a bad picklist value or an unknown field. Code &#x60;crm_validation_failed&#x60;; &#x60;details.errors&#x60; lists the CRM&#39;s own errors, each with &#x60;code&#x60;, &#x60;message&#x60; and the &#x60;fields&#x60; at fault when the CRM names them. |  -  |
| **429** | Zernio paces every connection inside its CRM limits (HubSpot per portal, Salesforce per org, HighLevel per location, shared with the conversation sync). Code &#x60;rate_limited&#x60;; wait for &#x60;Retry-After&#x60; seconds. |  * Retry-After - Seconds to wait before retrying. <br>  |
| **502** | The platform returned a server error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

