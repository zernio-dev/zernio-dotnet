# Zernio.Api.TrackingLinksApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTrackingLink**](TrackingLinksApi.md#createtrackinglink) | **POST** /v1/tracking-links | Create a tracking link |
| [**DeleteTrackingLink**](TrackingLinksApi.md#deletetrackinglink) | **DELETE** /v1/tracking-links/{linkId} | Delete a tracking link |
| [**GetTrackingLink**](TrackingLinksApi.md#gettrackinglink) | **GET** /v1/tracking-links/{linkId} | Get a tracking link |
| [**ListTrackingLinks**](TrackingLinksApi.md#listtrackinglinks) | **GET** /v1/tracking-links | List tracking links |
| [**RotateTrackingLinkPostbackToken**](TrackingLinksApi.md#rotatetrackinglinkpostbacktoken) | **POST** /v1/tracking-links/{linkId}/rotate-postback-token | Rotate a tracking link&#39;s postback URL |
| [**UpdateTrackingLink**](TrackingLinksApi.md#updatetrackinglink) | **PATCH** /v1/tracking-links/{linkId} | Update a tracking link |

<a id="createtrackinglink"></a>
# **CreateTrackingLink**
> CreateTrackingLink201Response CreateTrackingLink (string idempotencyKey, CreateTrackingLinkRequest createTrackingLinkRequest)

Create a tracking link

Creates a short link on a tracking site. Each click goes to one of `destinations`, picked by weight, so the link also split-tests landing pages. Put `url` in your ads and give `postbackUrl` to the network that reports conversions server to server. 

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
    public class CreateTrackingLinkExample
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
            var apiInstance = new TrackingLinksApi(httpClient, config, httpClientHandler);
            var idempotencyKey = "idempotencyKey_example";  // string | A unique key per link you create, such as a UUID. A retry with the same key and body returns the same link.
            var createTrackingLinkRequest = new CreateTrackingLinkRequest(); // CreateTrackingLinkRequest | 

            try
            {
                // Create a tracking link
                CreateTrackingLink201Response result = apiInstance.CreateTrackingLink(idempotencyKey, createTrackingLinkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingLinksApi.CreateTrackingLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrackingLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a tracking link
    ApiResponse<CreateTrackingLink201Response> response = apiInstance.CreateTrackingLinkWithHttpInfo(idempotencyKey, createTrackingLinkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingLinksApi.CreateTrackingLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **idempotencyKey** | **string** | A unique key per link you create, such as a UUID. A retry with the same key and body returns the same link. |  |
| **createTrackingLinkRequest** | [**CreateTrackingLinkRequest**](CreateTrackingLinkRequest.md) |  |  |

### Return type

[**CreateTrackingLink201Response**](CreateTrackingLink201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Link created. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No site with this id in your workspace (code &#x60;tracking_site_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletetrackinglink"></a>
# **DeleteTrackingLink**
> void DeleteTrackingLink (string linkId)

Delete a tracking link

The link and its postback URL stop working at once. Conversions already stored are kept.

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
    public class DeleteTrackingLinkExample
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
            var apiInstance = new TrackingLinksApi(httpClient, config, httpClientHandler);
            var linkId = "linkId_example";  // string | 

            try
            {
                // Delete a tracking link
                apiInstance.DeleteTrackingLink(linkId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingLinksApi.DeleteTrackingLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTrackingLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a tracking link
    apiInstance.DeleteTrackingLinkWithHttpInfo(linkId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingLinksApi.DeleteTrackingLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **linkId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Link deleted. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackinglink"></a>
# **GetTrackingLink**
> CreateTrackingLink201Response GetTrackingLink (string linkId)

Get a tracking link

One link, with its URL and postback URL.

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
    public class GetTrackingLinkExample
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
            var apiInstance = new TrackingLinksApi(httpClient, config, httpClientHandler);
            var linkId = "linkId_example";  // string | 

            try
            {
                // Get a tracking link
                CreateTrackingLink201Response result = apiInstance.GetTrackingLink(linkId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingLinksApi.GetTrackingLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a tracking link
    ApiResponse<CreateTrackingLink201Response> response = apiInstance.GetTrackingLinkWithHttpInfo(linkId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingLinksApi.GetTrackingLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **linkId** | **string** |  |  |

### Return type

[**CreateTrackingLink201Response**](CreateTrackingLink201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The link. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | No link with this id in your workspace (code &#x60;tracking_link_not_found&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackinglinks"></a>
# **ListTrackingLinks**
> ListTrackingLinks200Response ListTrackingLinks (string? profileId = null, string? siteId = null, int? limit = null, string? cursor = null)

List tracking links

The tracking links of your workspace in creation order. Pass `profileId` or `siteId` to list one profile's or one site's links.

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
    public class ListTrackingLinksExample
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
            var apiInstance = new TrackingLinksApi(httpClient, config, httpClientHandler);
            var profileId = "profileId_example";  // string? |  (optional) 
            var siteId = "siteId_example";  // string? |  (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? | `pagination.nextCursor` from the previous page. (optional) 

            try
            {
                // List tracking links
                ListTrackingLinks200Response result = apiInstance.ListTrackingLinks(profileId, siteId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingLinksApi.ListTrackingLinks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingLinksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List tracking links
    ApiResponse<ListTrackingLinks200Response> response = apiInstance.ListTrackingLinksWithHttpInfo(profileId, siteId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingLinksApi.ListTrackingLinksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string?** |  | [optional]  |
| **siteId** | **string?** |  | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** | &#x60;pagination.nextCursor&#x60; from the previous page. | [optional]  |

### Return type

[**ListTrackingLinks200Response**](ListTrackingLinks200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | One page of links. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="rotatetrackinglinkpostbacktoken"></a>
# **RotateTrackingLinkPostbackToken**
> CreateTrackingLink201Response RotateTrackingLinkPostbackToken (string linkId, string idempotencyKey)

Rotate a tracking link's postback URL

Issues a new `postbackUrl`. The old one stops working at once, so update it at the network right after.

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
    public class RotateTrackingLinkPostbackTokenExample
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
            var apiInstance = new TrackingLinksApi(httpClient, config, httpClientHandler);
            var linkId = "linkId_example";  // string | 
            var idempotencyKey = "idempotencyKey_example";  // string | A unique key per rotation, such as a UUID.

            try
            {
                // Rotate a tracking link's postback URL
                CreateTrackingLink201Response result = apiInstance.RotateTrackingLinkPostbackToken(linkId, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingLinksApi.RotateTrackingLinkPostbackToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RotateTrackingLinkPostbackTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rotate a tracking link's postback URL
    ApiResponse<CreateTrackingLink201Response> response = apiInstance.RotateTrackingLinkPostbackTokenWithHttpInfo(linkId, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingLinksApi.RotateTrackingLinkPostbackTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **linkId** | **string** |  |  |
| **idempotencyKey** | **string** | A unique key per rotation, such as a UUID. |  |

### Return type

[**CreateTrackingLink201Response**](CreateTrackingLink201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The link with its new postback URL. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetrackinglink"></a>
# **UpdateTrackingLink**
> CreateTrackingLink201Response UpdateTrackingLink (string linkId, UpdateTrackingLinkRequest updateTrackingLinkRequest)

Update a tracking link

Changes the link's name, destinations, campaign hints or status. Send at least one field. `status: paused` turns the link off until it is set back to `active`. `campaign: null` removes the hints. The code and URL never change. 

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
    public class UpdateTrackingLinkExample
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
            var apiInstance = new TrackingLinksApi(httpClient, config, httpClientHandler);
            var linkId = "linkId_example";  // string | 
            var updateTrackingLinkRequest = new UpdateTrackingLinkRequest(); // UpdateTrackingLinkRequest | 

            try
            {
                // Update a tracking link
                CreateTrackingLink201Response result = apiInstance.UpdateTrackingLink(linkId, updateTrackingLinkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingLinksApi.UpdateTrackingLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrackingLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a tracking link
    ApiResponse<CreateTrackingLink201Response> response = apiInstance.UpdateTrackingLinkWithHttpInfo(linkId, updateTrackingLinkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingLinksApi.UpdateTrackingLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **linkId** | **string** |  |  |
| **updateTrackingLinkRequest** | [**UpdateTrackingLinkRequest**](UpdateTrackingLinkRequest.md) |  |  |

### Return type

[**CreateTrackingLink201Response**](CreateTrackingLink201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated link. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

