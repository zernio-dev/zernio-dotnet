# Zernio.Api.LeadFormsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateLeadForm**](LeadFormsApi.md#createleadform) | **POST** /v1/ads/lead-forms | Create a Meta Lead Gen Form |
| [**CreateLeadFormTestLead**](LeadFormsApi.md#createleadformtestlead) | **POST** /v1/ads/lead-forms/{formId}/test-leads | Create a synthetic test lead |
| [**DeleteLeadForm**](LeadFormsApi.md#deleteleadform) | **DELETE** /v1/ads/lead-forms/{formId} | Delete a Lead Gen Form |
| [**DeleteLeadFormTestLead**](LeadFormsApi.md#deleteleadformtestlead) | **DELETE** /v1/ads/lead-forms/{formId}/test-leads/{leadId} | Delete a (test) lead |
| [**GetLeadForm**](LeadFormsApi.md#getleadform) | **GET** /v1/ads/lead-forms/{formId} | Get a Lead Gen Form |
| [**ListLeadFormLeads**](LeadFormsApi.md#listleadformleads) | **GET** /v1/ads/lead-forms/{formId}/leads | List submitted leads for a form |
| [**ListLeadForms**](LeadFormsApi.md#listleadforms) | **GET** /v1/ads/lead-forms | List Meta Lead Gen Forms |
| [**UpdateLeadForm**](LeadFormsApi.md#updateleadform) | **PATCH** /v1/ads/lead-forms/{formId} | Update a Lead Gen Form (status only) |

<a id="createleadform"></a>
# **CreateLeadForm**
> CreateLeadForm201Response CreateLeadForm (CreateLeadFormBody createLeadFormBody)

Create a Meta Lead Gen Form

Creates a new Instant Form on the Facebook Page tied to the given social account. The form is created in `ACTIVE` status and is immediately attachable to ads (see `leadGenFormId` on POST /v1/ads/create).  Once a form has received any leads, its questions / privacy policy / thank-you page become immutable on Meta's side; only `status` may be changed via PATCH. 

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
    public class CreateLeadFormExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var createLeadFormBody = new CreateLeadFormBody(); // CreateLeadFormBody | 

            try
            {
                // Create a Meta Lead Gen Form
                CreateLeadForm201Response result = apiInstance.CreateLeadForm(createLeadFormBody);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.CreateLeadForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateLeadFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a Meta Lead Gen Form
    ApiResponse<CreateLeadForm201Response> response = apiInstance.CreateLeadFormWithHttpInfo(createLeadFormBody);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.CreateLeadFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createLeadFormBody** | [**CreateLeadFormBody**](CreateLeadFormBody.md) |  |  |

### Return type

[**CreateLeadForm201Response**](CreateLeadForm201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Form created |  -  |
| **400** | Validation failure |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **404** | Social account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createleadformtestlead"></a>
# **CreateLeadFormTestLead**
> CreateLeadFormTestLead200Response CreateLeadFormTestLead (string formId, CreateLeadFormTestLeadRequest createLeadFormTestLeadRequest)

Create a synthetic test lead

Submits a fake lead against a form. Useful for QA, App Review demos, and exercising webhook subscribers without waiting for real ad impressions. Meta caps a form to one outstanding test lead — call DELETE on the returned id before re-submitting. 

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
    public class CreateLeadFormTestLeadExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var createLeadFormTestLeadRequest = new CreateLeadFormTestLeadRequest(); // CreateLeadFormTestLeadRequest | 

            try
            {
                // Create a synthetic test lead
                CreateLeadFormTestLead200Response result = apiInstance.CreateLeadFormTestLead(formId, createLeadFormTestLeadRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.CreateLeadFormTestLead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateLeadFormTestLeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a synthetic test lead
    ApiResponse<CreateLeadFormTestLead200Response> response = apiInstance.CreateLeadFormTestLeadWithHttpInfo(formId, createLeadFormTestLeadRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.CreateLeadFormTestLeadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string** |  |  |
| **createLeadFormTestLeadRequest** | [**CreateLeadFormTestLeadRequest**](CreateLeadFormTestLeadRequest.md) |  |  |

### Return type

[**CreateLeadFormTestLead200Response**](CreateLeadFormTestLead200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Test lead created |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **404** | Form or account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteleadform"></a>
# **DeleteLeadForm**
> DeleteLeadForm200Response DeleteLeadForm (string formId, string accountId)

Delete a Lead Gen Form

Deletes the form from Meta. If the form has already received leads, Meta archives it instead of hard-deleting; the response is the same either way. 

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
    public class DeleteLeadFormExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete a Lead Gen Form
                DeleteLeadForm200Response result = apiInstance.DeleteLeadForm(formId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.DeleteLeadForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteLeadFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a Lead Gen Form
    ApiResponse<DeleteLeadForm200Response> response = apiInstance.DeleteLeadFormWithHttpInfo(formId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.DeleteLeadFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**DeleteLeadForm200Response**](DeleteLeadForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Form deleted (or archived) |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **404** | Form not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteleadformtestlead"></a>
# **DeleteLeadFormTestLead**
> DeleteLeadForm200Response DeleteLeadFormTestLead (string formId, string leadId, string accountId)

Delete a (test) lead

Deletes a single lead by ID. Primarily used to clear the outstanding test lead so you can submit a new one. The same Graph API call works on real leads too; for production lead deletion (GDPR/CCPA) prefer a dedicated flow. 

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
    public class DeleteLeadFormTestLeadExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var leadId = "leadId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Delete a (test) lead
                DeleteLeadForm200Response result = apiInstance.DeleteLeadFormTestLead(formId, leadId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.DeleteLeadFormTestLead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteLeadFormTestLeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a (test) lead
    ApiResponse<DeleteLeadForm200Response> response = apiInstance.DeleteLeadFormTestLeadWithHttpInfo(formId, leadId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.DeleteLeadFormTestLeadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string** |  |  |
| **leadId** | **string** |  |  |
| **accountId** | **string** |  |  |

### Return type

[**DeleteLeadForm200Response**](DeleteLeadForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Lead deleted |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **404** | Lead not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getleadform"></a>
# **GetLeadForm**
> GetLeadForm200Response GetLeadForm (string formId, string accountId)

Get a Lead Gen Form

Returns full details for a single form, including questions, privacy policy, and lead counts.

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
    public class GetLeadFormExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | Meta lead form ID (numeric string)
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get a Lead Gen Form
                GetLeadForm200Response result = apiInstance.GetLeadForm(formId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.GetLeadForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLeadFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a Lead Gen Form
    ApiResponse<GetLeadForm200Response> response = apiInstance.GetLeadFormWithHttpInfo(formId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.GetLeadFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string** | Meta lead form ID (numeric string) |  |
| **accountId** | **string** |  |  |

### Return type

[**GetLeadForm200Response**](GetLeadForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Form details |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **404** | Form or account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listleadformleads"></a>
# **ListLeadFormLeads**
> ListLeadFormLeads200Response ListLeadFormLeads (string formId, string accountId, int? limit = null, string? cursor = null, int? since = null)

List submitted leads for a form

Returns leads submitted against a Lead Gen Form. The page access token on the connected account must have the `leads_retrieval` permission — if the token was minted before that scope was approved, this endpoint returns `code: scope_reconnect_required` (HTTP 422) and the customer must reconnect the Facebook account.  For real-time delivery without polling, subscribe a webhook to the `lead.received` event. 

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
    public class ListLeadFormLeadsExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? |  (optional) 
            var since = 56;  // int? | Unix timestamp; only return leads created strictly after this. (optional) 

            try
            {
                // List submitted leads for a form
                ListLeadFormLeads200Response result = apiInstance.ListLeadFormLeads(formId, accountId, limit, cursor, since);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.ListLeadFormLeads: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLeadFormLeadsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List submitted leads for a form
    ApiResponse<ListLeadFormLeads200Response> response = apiInstance.ListLeadFormLeadsWithHttpInfo(formId, accountId, limit, cursor, since);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.ListLeadFormLeadsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string** |  |  |
| **accountId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** |  | [optional]  |
| **since** | **int?** | Unix timestamp; only return leads created strictly after this. | [optional]  |

### Return type

[**ListLeadFormLeads200Response**](ListLeadFormLeads200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Leads |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **422** | Connected account is missing the &#x60;leads_retrieval&#x60; scope and must be reconnected. &#x60;code&#x60; is &#x60;scope_reconnect_required&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listleadforms"></a>
# **ListLeadForms**
> ListLeadForms200Response ListLeadForms (string accountId, int? limit = null, string? cursor = null)

List Meta Lead Gen Forms

Returns Meta Instant Forms attached to the Facebook Page connected via the given social account. Forms live on Facebook Pages — Instagram lead ads reuse the linked Page under the hood, so even Instagram-only ad accounts list forms from the linked Facebook Page. Requires the Ads add-on. 

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
    public class ListLeadFormsExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Facebook social account ID (Late SocialAccount _id)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? | Meta `paging.cursors.after` from a prior page (optional) 

            try
            {
                // List Meta Lead Gen Forms
                ListLeadForms200Response result = apiInstance.ListLeadForms(accountId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.ListLeadForms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLeadFormsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Meta Lead Gen Forms
    ApiResponse<ListLeadForms200Response> response = apiInstance.ListLeadFormsWithHttpInfo(accountId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.ListLeadFormsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Facebook social account ID (Late SocialAccount _id) |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** | Meta &#x60;paging.cursors.after&#x60; from a prior page | [optional]  |

### Return type

[**ListLeadForms200Response**](ListLeadForms200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Forms list |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **404** | Social account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateleadform"></a>
# **UpdateLeadForm**
> DeleteLeadForm200Response UpdateLeadForm (string formId, UpdateLeadFormRequest updateLeadFormRequest)

Update a Lead Gen Form (status only)

Update mutable fields on an existing form. Today only `status` is mutable on Meta's side — questions / privacy_policy / thank_you_page are immutable once a form has received any leads. 

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
    public class UpdateLeadFormExample
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
            var apiInstance = new LeadFormsApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var updateLeadFormRequest = new UpdateLeadFormRequest(); // UpdateLeadFormRequest | 

            try
            {
                // Update a Lead Gen Form (status only)
                DeleteLeadForm200Response result = apiInstance.UpdateLeadForm(formId, updateLeadFormRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadFormsApi.UpdateLeadForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateLeadFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a Lead Gen Form (status only)
    ApiResponse<DeleteLeadForm200Response> response = apiInstance.UpdateLeadFormWithHttpInfo(formId, updateLeadFormRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadFormsApi.UpdateLeadFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string** |  |  |
| **updateLeadFormRequest** | [**UpdateLeadFormRequest**](UpdateLeadFormRequest.md) |  |  |

### Return type

[**DeleteLeadForm200Response**](DeleteLeadForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Form updated |  -  |
| **400** | Validation failure |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required |  -  |
| **404** | Form not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

