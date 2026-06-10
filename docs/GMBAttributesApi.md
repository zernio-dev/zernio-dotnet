# Zernio.Api.GMBAttributesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetGmbAttributeMetadata**](GMBAttributesApi.md#getgmbattributemetadata) | **GET** /v1/accounts/{accountId}/gmb-attribute-metadata | Get attribute metadata |
| [**GetGoogleBusinessAttributes**](GMBAttributesApi.md#getgooglebusinessattributes) | **GET** /v1/accounts/{accountId}/gmb-attributes | Get attributes |
| [**UpdateGoogleBusinessAttributes**](GMBAttributesApi.md#updategooglebusinessattributes) | **PUT** /v1/accounts/{accountId}/gmb-attributes | Update attributes |

<a id="getgmbattributemetadata"></a>
# **GetGmbAttributeMetadata**
> GetGmbAttributeMetadata200Response GetGmbAttributeMetadata (string accountId, string? locationId = null, string? categoryName = null, string? regionCode = null, string? languageCode = null, int? pageSize = null, string? pageToken = null)

Get attribute metadata

Returns metadata about which Google Business Profile attributes are available for a location or business category. Use this endpoint to discover valid attribute names, value types, and allowed enum values before reading or writing via gmb-attributes.  Two mutually exclusive query modes:  **Location mode**: pass `locationId` (or rely on the account's stored `selectedLocationId`). Google returns attributes valid for that specific location.  **Category mode**: pass `categoryName` (must start with `categories/`) and `regionCode`. Google returns attributes valid for that category across the given region. `languageCode` is optional in category mode.  Both modes support `pageSize` and `pageToken` for pagination. 

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
    public class GetGmbAttributeMetadataExample
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
            var apiInstance = new GMBAttributesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var locationId = "locationId_example";  // string? | GBP location ID (e.g. \"6257659026299438786\"). If omitted, uses the account's stored selectedLocationId. Mutually exclusive with categoryName.  (optional) 
            var categoryName = "categoryName_example";  // string? | Category resource name, must start with \"categories/\" (e.g. \"categories/gcid:plumber\"). Required together with regionCode. Mutually exclusive with locationId.  (optional) 
            var regionCode = "regionCode_example";  // string? | BCP-47 region code (e.g. \"US\", \"ES\"). Required when categoryName is provided.  (optional) 
            var languageCode = "languageCode_example";  // string? | BCP-47 language code for display names (e.g. \"en\", \"es\"). Optional when categoryName is provided. Omitted from the Google call when not supplied.  (optional) 
            var pageSize = 56;  // int? | Maximum number of attribute metadata items to return. Google defaults to 200. (optional) 
            var pageToken = "pageToken_example";  // string? | Pagination token from a previous response's nextPageToken field. (optional) 

            try
            {
                // Get attribute metadata
                GetGmbAttributeMetadata200Response result = apiInstance.GetGmbAttributeMetadata(accountId, locationId, categoryName, regionCode, languageCode, pageSize, pageToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBAttributesApi.GetGmbAttributeMetadata: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGmbAttributeMetadataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get attribute metadata
    ApiResponse<GetGmbAttributeMetadata200Response> response = apiInstance.GetGmbAttributeMetadataWithHttpInfo(accountId, locationId, categoryName, regionCode, languageCode, pageSize, pageToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBAttributesApi.GetGmbAttributeMetadataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **locationId** | **string?** | GBP location ID (e.g. \&quot;6257659026299438786\&quot;). If omitted, uses the account&#39;s stored selectedLocationId. Mutually exclusive with categoryName.  | [optional]  |
| **categoryName** | **string?** | Category resource name, must start with \&quot;categories/\&quot; (e.g. \&quot;categories/gcid:plumber\&quot;). Required together with regionCode. Mutually exclusive with locationId.  | [optional]  |
| **regionCode** | **string?** | BCP-47 region code (e.g. \&quot;US\&quot;, \&quot;ES\&quot;). Required when categoryName is provided.  | [optional]  |
| **languageCode** | **string?** | BCP-47 language code for display names (e.g. \&quot;en\&quot;, \&quot;es\&quot;). Optional when categoryName is provided. Omitted from the Google call when not supplied.  | [optional]  |
| **pageSize** | **int?** | Maximum number of attribute metadata items to return. Google defaults to 200. | [optional]  |
| **pageToken** | **string?** | Pagination token from a previous response&#39;s nextPageToken field. | [optional]  |

### Return type

[**GetGmbAttributeMetadata200Response**](GetGmbAttributeMetadata200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Attribute metadata fetched successfully |  -  |
| **400** | Invalid request (mixed modes, missing required params, wrong platform, or Google returned 4xx) |  -  |
| **401** | Access token is invalid or revoked. Reconnect the Google Business Profile account. |  -  |
| **404** | Account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getgooglebusinessattributes"></a>
# **GetGoogleBusinessAttributes**
> GetGoogleBusinessAttributes200Response GetGoogleBusinessAttributes (string accountId, string? locationId = null)

Get attributes

Returns GBP location attributes (amenities, services, accessibility, payment types). Available attributes vary by business category.

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
    public class GetGoogleBusinessAttributesExample
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
            var apiInstance = new GMBAttributesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var locationId = "locationId_example";  // string? | Override which location to query. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. (optional) 

            try
            {
                // Get attributes
                GetGoogleBusinessAttributes200Response result = apiInstance.GetGoogleBusinessAttributes(accountId, locationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBAttributesApi.GetGoogleBusinessAttributes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGoogleBusinessAttributesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get attributes
    ApiResponse<GetGoogleBusinessAttributes200Response> response = apiInstance.GetGoogleBusinessAttributesWithHttpInfo(accountId, locationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBAttributesApi.GetGoogleBusinessAttributesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **locationId** | **string?** | Override which location to query. If omitted, uses the account&#39;s selected location. Use GET /gmb-locations to list valid IDs. | [optional]  |

### Return type

[**GetGoogleBusinessAttributes200Response**](GetGoogleBusinessAttributes200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Attributes fetched successfully |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updategooglebusinessattributes"></a>
# **UpdateGoogleBusinessAttributes**
> UpdateGoogleBusinessAttributes200Response UpdateGoogleBusinessAttributes (string accountId, UpdateGoogleBusinessAttributesRequest updateGoogleBusinessAttributesRequest, string? locationId = null)

Update attributes

Updates location attributes (amenities, services, etc.).  The attributeMask specifies which attributes to update (comma-separated). 

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
    public class UpdateGoogleBusinessAttributesExample
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
            var apiInstance = new GMBAttributesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var updateGoogleBusinessAttributesRequest = new UpdateGoogleBusinessAttributesRequest(); // UpdateGoogleBusinessAttributesRequest | 
            var locationId = "locationId_example";  // string? | Override which location to target. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. (optional) 

            try
            {
                // Update attributes
                UpdateGoogleBusinessAttributes200Response result = apiInstance.UpdateGoogleBusinessAttributes(accountId, updateGoogleBusinessAttributesRequest, locationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GMBAttributesApi.UpdateGoogleBusinessAttributes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateGoogleBusinessAttributesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update attributes
    ApiResponse<UpdateGoogleBusinessAttributes200Response> response = apiInstance.UpdateGoogleBusinessAttributesWithHttpInfo(accountId, updateGoogleBusinessAttributesRequest, locationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GMBAttributesApi.UpdateGoogleBusinessAttributesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **updateGoogleBusinessAttributesRequest** | [**UpdateGoogleBusinessAttributesRequest**](UpdateGoogleBusinessAttributesRequest.md) |  |  |
| **locationId** | **string?** | Override which location to target. If omitted, uses the account&#39;s selected location. Use GET /gmb-locations to list valid IDs. | [optional]  |

### Return type

[**UpdateGoogleBusinessAttributes200Response**](UpdateGoogleBusinessAttributes200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Attributes updated successfully |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

