# Zernio.Api.LeadGenApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveLeadForm**](LeadGenApi.md#archiveleadform) | **DELETE** /v1/ads/lead-forms/{formId} | Archive a lead form |
| [**CreateLeadForm**](LeadGenApi.md#createleadform) | **POST** /v1/ads/lead-forms | Create a lead form |
| [**CreateTestLead**](LeadGenApi.md#createtestlead) | **POST** /v1/ads/lead-forms/{formId}/test-leads | Create a test lead |
| [**GetLeadForm**](LeadGenApi.md#getleadform) | **GET** /v1/ads/lead-forms/{formId} | Get a lead form |
| [**ListFormLeads**](LeadGenApi.md#listformleads) | **GET** /v1/ads/lead-forms/{formId}/leads | List leads for a single form |
| [**ListLeadForms**](LeadGenApi.md#listleadforms) | **GET** /v1/ads/lead-forms | List lead forms |
| [**ListLeads**](LeadGenApi.md#listleads) | **GET** /v1/ads/leads | List submitted leads |

<a id="archiveleadform"></a>
# **ArchiveLeadForm**
> ArchiveLeadForm200Response ArchiveLeadForm (string formId, string accountId)

Archive a lead form

Meta has no hard delete for forms; this archives the form (status=ARCHIVED).

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
    public class ArchiveLeadFormExample
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
            var apiInstance = new LeadGenApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Archive a lead form
                ArchiveLeadForm200Response result = apiInstance.ArchiveLeadForm(formId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadGenApi.ArchiveLeadForm: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveLeadFormWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive a lead form
    ApiResponse<ArchiveLeadForm200Response> response = apiInstance.ArchiveLeadFormWithHttpInfo(formId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadGenApi.ArchiveLeadFormWithHttpInfo: " + e.Message);
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

[**ArchiveLeadForm200Response**](ArchiveLeadForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Archived. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createleadform"></a>
# **CreateLeadForm**
> CreateLeadForm200Response CreateLeadForm (CreateLeadFormRequest createLeadFormRequest)

Create a lead form

Creates a Lead Gen form on the connected Facebook Page (POST /{page-id}/leadgen_forms). NOT idempotent — a retry creates a second form. Prefilled question types (EMAIL, PHONE, FULL_NAME, …) must omit label/key; CUSTOM questions require both. Requires the Ads add-on. 

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
            var apiInstance = new LeadGenApi(httpClient, config, httpClientHandler);
            var createLeadFormRequest = new CreateLeadFormRequest(); // CreateLeadFormRequest | 

            try
            {
                // Create a lead form
                CreateLeadForm200Response result = apiInstance.CreateLeadForm(createLeadFormRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadGenApi.CreateLeadForm: " + e.Message);
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
    // Create a lead form
    ApiResponse<CreateLeadForm200Response> response = apiInstance.CreateLeadFormWithHttpInfo(createLeadFormRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadGenApi.CreateLeadFormWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createLeadFormRequest** | [**CreateLeadFormRequest**](CreateLeadFormRequest.md) |  |  |

### Return type

[**CreateLeadForm200Response**](CreateLeadForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Created form. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtestlead"></a>
# **CreateTestLead**
> CreateTestLead200Response CreateTestLead (string formId, CreateTestLeadRequest createTestLeadRequest)

Create a test lead

Submits a test lead against the form (POST /{form-id}/test_leads) to exercise retrieval without waiting for real ad impressions. Meta allows one test lead per form at a time. 

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
    public class CreateTestLeadExample
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
            var apiInstance = new LeadGenApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var createTestLeadRequest = new CreateTestLeadRequest(); // CreateTestLeadRequest | 

            try
            {
                // Create a test lead
                CreateTestLead200Response result = apiInstance.CreateTestLead(formId, createTestLeadRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadGenApi.CreateTestLead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTestLeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a test lead
    ApiResponse<CreateTestLead200Response> response = apiInstance.CreateTestLeadWithHttpInfo(formId, createTestLeadRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadGenApi.CreateTestLeadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string** |  |  |
| **createTestLeadRequest** | [**CreateTestLeadRequest**](CreateTestLeadRequest.md) |  |  |

### Return type

[**CreateTestLead200Response**](CreateTestLead200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Test lead created. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getleadform"></a>
# **GetLeadForm**
> GetLeadForm200Response GetLeadForm (string formId, string accountId)

Get a lead form

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
            var apiInstance = new LeadGenApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var accountId = "accountId_example";  // string | 

            try
            {
                // Get a lead form
                GetLeadForm200Response result = apiInstance.GetLeadForm(formId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadGenApi.GetLeadForm: " + e.Message);
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
    // Get a lead form
    ApiResponse<GetLeadForm200Response> response = apiInstance.GetLeadFormWithHttpInfo(formId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadGenApi.GetLeadFormWithHttpInfo: " + e.Message);
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

[**GetLeadForm200Response**](GetLeadForm200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Form metadata. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listformleads"></a>
# **ListFormLeads**
> ListFormLeads200Response ListFormLeads (string formId, string accountId, int? limit = null, string? cursor = null, int? since = null)

List leads for a single form

Returns leads for one form. Serves persisted leads (ingested via the leadgen webhook) when available, falling back to a live Graph read. 

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
    public class ListFormLeadsExample
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
            var apiInstance = new LeadGenApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string | 
            var accountId = "accountId_example";  // string | 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? |  (optional) 
            var since = 56;  // int? | Unix seconds. (optional) 

            try
            {
                // List leads for a single form
                ListFormLeads200Response result = apiInstance.ListFormLeads(formId, accountId, limit, cursor, since);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadGenApi.ListFormLeads: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListFormLeadsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List leads for a single form
    ApiResponse<ListFormLeads200Response> response = apiInstance.ListFormLeadsWithHttpInfo(formId, accountId, limit, cursor, since);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadGenApi.ListFormLeadsWithHttpInfo: " + e.Message);
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
| **since** | **int?** | Unix seconds. | [optional]  |

### Return type

[**ListFormLeads200Response**](ListFormLeads200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Leads for the form. |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listleadforms"></a>
# **ListLeadForms**
> ListLeadForms200Response ListLeadForms (string accountId, int? limit = null, string? cursor = null)

List lead forms

Lists the Lead Gen forms owned by the connected Facebook Page. Requires the Ads add-on.

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
            var apiInstance = new LeadGenApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected facebook account id.
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List lead forms
                ListLeadForms200Response result = apiInstance.ListLeadForms(accountId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadGenApi.ListLeadForms: " + e.Message);
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
    // List lead forms
    ApiResponse<ListLeadForms200Response> response = apiInstance.ListLeadFormsWithHttpInfo(accountId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadGenApi.ListLeadFormsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected facebook account id. |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** |  | [optional]  |

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
| **200** | Forms list. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listleads"></a>
# **ListLeads**
> ListLeads200Response ListLeads (string? formId = null, string? accountId = null, int? limit = null, int? since = null, string? cursor = null)

List submitted leads

Returns persisted Meta Lead Gen leads for your team, newest-first, with keyset pagination on `cursor`. Leads are ingested in real time from the `leadgen` webhook. Requires the Ads add-on. 

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
    public class ListLeadsExample
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
            var apiInstance = new LeadGenApi(httpClient, config, httpClientHandler);
            var formId = "formId_example";  // string? | Filter to a single lead form. (optional) 
            var accountId = "accountId_example";  // string? | Filter to a single connected account. (optional) 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var since = 56;  // int? | Unix seconds; only leads created at/after this Meta timestamp. (optional) 
            var cursor = "cursor_example";  // string? | Keyset cursor from a previous response's pagination.cursor. (optional) 

            try
            {
                // List submitted leads
                ListLeads200Response result = apiInstance.ListLeads(formId, accountId, limit, since, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LeadGenApi.ListLeads: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLeadsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List submitted leads
    ApiResponse<ListLeads200Response> response = apiInstance.ListLeadsWithHttpInfo(formId, accountId, limit, since, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LeadGenApi.ListLeadsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **formId** | **string?** | Filter to a single lead form. | [optional]  |
| **accountId** | **string?** | Filter to a single connected account. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **since** | **int?** | Unix seconds; only leads created at/after this Meta timestamp. | [optional]  |
| **cursor** | **string?** | Keyset cursor from a previous response&#39;s pagination.cursor. | [optional]  |

### Return type

[**ListLeads200Response**](ListLeads200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Lead list. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

