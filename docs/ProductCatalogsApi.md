# Zernio.Api.ProductCatalogsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BatchAdCatalogProducts**](ProductCatalogsApi.md#batchadcatalogproducts) | **POST** /v1/ads/catalogs/{catalogId}/products/batch | Create, update or delete products in bulk |
| [**CreateAdCatalog**](ProductCatalogsApi.md#createadcatalog) | **POST** /v1/ads/catalogs | Create a Meta product catalog |
| [**CreateAdCatalogFeed**](ProductCatalogsApi.md#createadcatalogfeed) | **POST** /v1/ads/catalogs/{catalogId}/feeds | Create a product feed |
| [**CreateAdCatalogFeedUpload**](ProductCatalogsApi.md#createadcatalogfeedupload) | **POST** /v1/ads/catalogs/{catalogId}/feeds/{feedId}/uploads | Fetch a feed file now |
| [**CreateAdCatalogProduct**](ProductCatalogsApi.md#createadcatalogproduct) | **POST** /v1/ads/catalogs/{catalogId}/products | Add a product to a catalog |
| [**CreateAdCatalogProductSet**](ProductCatalogsApi.md#createadcatalogproductset) | **POST** /v1/ads/catalogs/{catalogId}/product-sets | Create a product set |
| [**DeleteAdCatalog**](ProductCatalogsApi.md#deleteadcatalog) | **DELETE** /v1/ads/catalogs/{catalogId} | Delete a product catalog |
| [**DeleteAdCatalogProduct**](ProductCatalogsApi.md#deleteadcatalogproduct) | **DELETE** /v1/ads/catalogs/{catalogId}/products/{productId} | Delete a product |
| [**DeleteAdCatalogProductSet**](ProductCatalogsApi.md#deleteadcatalogproductset) | **DELETE** /v1/ads/catalogs/{catalogId}/product-sets/{productSetId} | Delete a product set |
| [**GetAdCatalog**](ProductCatalogsApi.md#getadcatalog) | **GET** /v1/ads/catalogs/{catalogId} | Get a product catalog |
| [**GetAdCatalogBatch**](ProductCatalogsApi.md#getadcatalogbatch) | **GET** /v1/ads/catalogs/{catalogId}/batches/{handle} | Get a bulk request&#39;s status |
| [**GetAdCatalogProduct**](ProductCatalogsApi.md#getadcatalogproduct) | **GET** /v1/ads/catalogs/{catalogId}/products/{productId} | Get a product |
| [**ListAdCatalogFeedUploads**](ProductCatalogsApi.md#listadcatalogfeeduploads) | **GET** /v1/ads/catalogs/{catalogId}/feeds/{feedId}/uploads | List a feed&#39;s uploads |
| [**ListAdCatalogFeeds**](ProductCatalogsApi.md#listadcatalogfeeds) | **GET** /v1/ads/catalogs/{catalogId}/feeds | List a catalog&#39;s product feeds |
| [**ListAdCatalogProductSets**](ProductCatalogsApi.md#listadcatalogproductsets) | **GET** /v1/ads/catalogs/{catalogId}/product-sets | List a catalog&#39;s product sets |
| [**ListAdCatalogProducts**](ProductCatalogsApi.md#listadcatalogproducts) | **GET** /v1/ads/catalogs/{catalogId}/products | List a catalog&#39;s products |
| [**ListAdCatalogs**](ProductCatalogsApi.md#listadcatalogs) | **GET** /v1/ads/catalogs | List Meta product catalogs |
| [**UpdateAdCatalogProduct**](ProductCatalogsApi.md#updateadcatalogproduct) | **PUT** /v1/ads/catalogs/{catalogId}/products/{productId} | Update a product |
| [**UpdateAdCatalogProductSet**](ProductCatalogsApi.md#updateadcatalogproductset) | **PUT** /v1/ads/catalogs/{catalogId}/product-sets/{productSetId} | Update a product set |

<a id="batchadcatalogproducts"></a>
# **BatchAdCatalogProducts**
> BatchAdCatalogProducts202Response BatchAdCatalogProducts (string catalogId, BatchAdCatalogProductsRequest batchAdCatalogProductsRequest)

Create, update or delete products in bulk

Up to 5000 CREATE / UPDATE / DELETE requests keyed by `retailerId`, processed asynchronously by Meta. Returns handles; poll GET /v1/ads/catalogs/{catalogId}/batches/{handle} for the outcome and per-item errors. CREATE requests need name, url, imageUrl, price and currency.

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
    public class BatchAdCatalogProductsExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var batchAdCatalogProductsRequest = new BatchAdCatalogProductsRequest(); // BatchAdCatalogProductsRequest | 

            try
            {
                // Create, update or delete products in bulk
                BatchAdCatalogProducts202Response result = apiInstance.BatchAdCatalogProducts(catalogId, batchAdCatalogProductsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.BatchAdCatalogProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BatchAdCatalogProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create, update or delete products in bulk
    ApiResponse<BatchAdCatalogProducts202Response> response = apiInstance.BatchAdCatalogProductsWithHttpInfo(catalogId, batchAdCatalogProductsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.BatchAdCatalogProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **batchAdCatalogProductsRequest** | [**BatchAdCatalogProductsRequest**](BatchAdCatalogProductsRequest.md) |  |  |

### Return type

[**BatchAdCatalogProducts202Response**](BatchAdCatalogProducts202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Accepted by Meta |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcatalog"></a>
# **CreateAdCatalog**
> CreateAdCatalog201Response CreateAdCatalog (CreateAdCatalogRequest createAdCatalogRequest)

Create a Meta product catalog

Creates a Meta Commerce catalog in the business portfolio (resolved like GET). The same catalog serves Advantage+ catalog ads, Instagram/Facebook Shops and the WhatsApp Business catalog: link it to a WhatsApp number with POST /v1/whatsapp/catalogs. Needs catalog_management on the Meta login.

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
    public class CreateAdCatalogExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var createAdCatalogRequest = new CreateAdCatalogRequest(); // CreateAdCatalogRequest | 

            try
            {
                // Create a Meta product catalog
                CreateAdCatalog201Response result = apiInstance.CreateAdCatalog(createAdCatalogRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCatalogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a Meta product catalog
    ApiResponse<CreateAdCatalog201Response> response = apiInstance.CreateAdCatalogWithHttpInfo(createAdCatalogRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdCatalogRequest** | [**CreateAdCatalogRequest**](CreateAdCatalogRequest.md) |  |  |

### Return type

[**CreateAdCatalog201Response**](CreateAdCatalog201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Catalog created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcatalogfeed"></a>
# **CreateAdCatalogFeed**
> CreateAdCatalogFeed201Response CreateAdCatalogFeed (string catalogId, CreateAdCatalogFeedRequest createAdCatalogFeedRequest)

Create a product feed

A feed pulls a CSV/TSV/XML product file from a URL. With `schedule` Meta fetches it on a cadence; without it, trigger fetches with POST /v1/ads/catalogs/{catalogId}/feeds/{feedId}/uploads.

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
    public class CreateAdCatalogFeedExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var createAdCatalogFeedRequest = new CreateAdCatalogFeedRequest(); // CreateAdCatalogFeedRequest | 

            try
            {
                // Create a product feed
                CreateAdCatalogFeed201Response result = apiInstance.CreateAdCatalogFeed(catalogId, createAdCatalogFeedRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogFeed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCatalogFeedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a product feed
    ApiResponse<CreateAdCatalogFeed201Response> response = apiInstance.CreateAdCatalogFeedWithHttpInfo(catalogId, createAdCatalogFeedRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogFeedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **createAdCatalogFeedRequest** | [**CreateAdCatalogFeedRequest**](CreateAdCatalogFeedRequest.md) |  |  |

### Return type

[**CreateAdCatalogFeed201Response**](CreateAdCatalogFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Feed created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcatalogfeedupload"></a>
# **CreateAdCatalogFeedUpload**
> CreateAdCatalogFeedUpload202Response CreateAdCatalogFeedUpload (string catalogId, string feedId, CreateAdCatalogFeedUploadRequest createAdCatalogFeedUploadRequest)

Fetch a feed file now

Asks Meta to fetch the product file at `url` into the feed. Processing is asynchronous: read the outcome with GET uploads.

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
    public class CreateAdCatalogFeedUploadExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var feedId = "feedId_example";  // string | 
            var createAdCatalogFeedUploadRequest = new CreateAdCatalogFeedUploadRequest(); // CreateAdCatalogFeedUploadRequest | 

            try
            {
                // Fetch a feed file now
                CreateAdCatalogFeedUpload202Response result = apiInstance.CreateAdCatalogFeedUpload(catalogId, feedId, createAdCatalogFeedUploadRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogFeedUpload: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCatalogFeedUploadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Fetch a feed file now
    ApiResponse<CreateAdCatalogFeedUpload202Response> response = apiInstance.CreateAdCatalogFeedUploadWithHttpInfo(catalogId, feedId, createAdCatalogFeedUploadRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogFeedUploadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **feedId** | **string** |  |  |
| **createAdCatalogFeedUploadRequest** | [**CreateAdCatalogFeedUploadRequest**](CreateAdCatalogFeedUploadRequest.md) |  |  |

### Return type

[**CreateAdCatalogFeedUpload202Response**](CreateAdCatalogFeedUpload202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Fetch started |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcatalogproduct"></a>
# **CreateAdCatalogProduct**
> CreateAdCatalogProduct201Response CreateAdCatalogProduct (string catalogId, CreateAdCatalogProductRequest createAdCatalogProductRequest)

Add a product to a catalog

Adds one product. `retailerId` is your SKU and stays the handle for later lookups and batch updates. For many products at once use POST /v1/ads/catalogs/{catalogId}/products/batch. Needs catalog_management on the Meta login.

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
    public class CreateAdCatalogProductExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var createAdCatalogProductRequest = new CreateAdCatalogProductRequest(); // CreateAdCatalogProductRequest | 

            try
            {
                // Add a product to a catalog
                CreateAdCatalogProduct201Response result = apiInstance.CreateAdCatalogProduct(catalogId, createAdCatalogProductRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCatalogProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add a product to a catalog
    ApiResponse<CreateAdCatalogProduct201Response> response = apiInstance.CreateAdCatalogProductWithHttpInfo(catalogId, createAdCatalogProductRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **createAdCatalogProductRequest** | [**CreateAdCatalogProductRequest**](CreateAdCatalogProductRequest.md) |  |  |

### Return type

[**CreateAdCatalogProduct201Response**](CreateAdCatalogProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcatalogproductset"></a>
# **CreateAdCatalogProductSet**
> CreateAdCatalogProductSet201Response CreateAdCatalogProductSet (string catalogId, CreateAdCatalogProductSetRequest createAdCatalogProductSetRequest)

Create a product set

A product set is a filter over the catalog, e.g. `{\"retailer_id\": {\"is_any\": [\"sku-1\", \"sku-2\"]}}` or `{\"brand\": {\"i_contains\": \"acme\"}}` (Meta's product set filter syntax).

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
    public class CreateAdCatalogProductSetExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var createAdCatalogProductSetRequest = new CreateAdCatalogProductSetRequest(); // CreateAdCatalogProductSetRequest | 

            try
            {
                // Create a product set
                CreateAdCatalogProductSet201Response result = apiInstance.CreateAdCatalogProductSet(catalogId, createAdCatalogProductSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogProductSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCatalogProductSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a product set
    ApiResponse<CreateAdCatalogProductSet201Response> response = apiInstance.CreateAdCatalogProductSetWithHttpInfo(catalogId, createAdCatalogProductSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.CreateAdCatalogProductSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **createAdCatalogProductSetRequest** | [**CreateAdCatalogProductSetRequest**](CreateAdCatalogProductSetRequest.md) |  |  |

### Return type

[**CreateAdCatalogProductSet201Response**](CreateAdCatalogProductSet201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product set created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadcatalog"></a>
# **DeleteAdCatalog**
> DeleteAdCatalog200Response DeleteAdCatalog (string catalogId, string accountId, string? catalogAccountId = null)

Delete a product catalog

Deletes the catalog and every product in it on Meta. Ads and WhatsApp numbers that use it lose their catalog.

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
    public class DeleteAdCatalogExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // Delete a product catalog
                DeleteAdCatalog200Response result = apiInstance.DeleteAdCatalog(catalogId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.DeleteAdCatalog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdCatalogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a product catalog
    ApiResponse<DeleteAdCatalog200Response> response = apiInstance.DeleteAdCatalogWithHttpInfo(catalogId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.DeleteAdCatalogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**DeleteAdCatalog200Response**](DeleteAdCatalog200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadcatalogproduct"></a>
# **DeleteAdCatalogProduct**
> DeleteAdCatalogProduct200Response DeleteAdCatalogProduct (string catalogId, string productId, string accountId, string? catalogAccountId = null)

Delete a product

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
    public class DeleteAdCatalogProductExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var productId = "productId_example";  // string | Meta product item ID (from the products list; not the retailer id)
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // Delete a product
                DeleteAdCatalogProduct200Response result = apiInstance.DeleteAdCatalogProduct(catalogId, productId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.DeleteAdCatalogProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdCatalogProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a product
    ApiResponse<DeleteAdCatalogProduct200Response> response = apiInstance.DeleteAdCatalogProductWithHttpInfo(catalogId, productId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.DeleteAdCatalogProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **productId** | **string** | Meta product item ID (from the products list; not the retailer id) |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**DeleteAdCatalogProduct200Response**](DeleteAdCatalogProduct200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadcatalogproductset"></a>
# **DeleteAdCatalogProductSet**
> DeleteAdCatalogProductSet200Response DeleteAdCatalogProductSet (string catalogId, string productSetId, string accountId, string? catalogAccountId = null)

Delete a product set

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
    public class DeleteAdCatalogProductSetExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var productSetId = "productSetId_example";  // string | 
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // Delete a product set
                DeleteAdCatalogProductSet200Response result = apiInstance.DeleteAdCatalogProductSet(catalogId, productSetId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.DeleteAdCatalogProductSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdCatalogProductSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a product set
    ApiResponse<DeleteAdCatalogProductSet200Response> response = apiInstance.DeleteAdCatalogProductSetWithHttpInfo(catalogId, productSetId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.DeleteAdCatalogProductSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **productSetId** | **string** |  |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**DeleteAdCatalogProductSet200Response**](DeleteAdCatalogProductSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcatalog"></a>
# **GetAdCatalog**
> CreateAdCatalog201Response GetAdCatalog (string catalogId, string accountId, string? catalogAccountId = null)

Get a product catalog

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
    public class GetAdCatalogExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // Get a product catalog
                CreateAdCatalog201Response result = apiInstance.GetAdCatalog(catalogId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.GetAdCatalog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCatalogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a product catalog
    ApiResponse<CreateAdCatalog201Response> response = apiInstance.GetAdCatalogWithHttpInfo(catalogId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.GetAdCatalogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**CreateAdCatalog201Response**](CreateAdCatalog201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcatalogbatch"></a>
# **GetAdCatalogBatch**
> GetAdCatalogBatch200Response GetAdCatalogBatch (string catalogId, string handle, string accountId, string? catalogAccountId = null)

Get a bulk request's status

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
    public class GetAdCatalogBatchExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var handle = "handle_example";  // string | Handle returned by the batch call
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // Get a bulk request's status
                GetAdCatalogBatch200Response result = apiInstance.GetAdCatalogBatch(catalogId, handle, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.GetAdCatalogBatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCatalogBatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a bulk request's status
    ApiResponse<GetAdCatalogBatch200Response> response = apiInstance.GetAdCatalogBatchWithHttpInfo(catalogId, handle, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.GetAdCatalogBatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **handle** | **string** | Handle returned by the batch call |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**GetAdCatalogBatch200Response**](GetAdCatalogBatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Batch status |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcatalogproduct"></a>
# **GetAdCatalogProduct**
> CreateAdCatalogProduct201Response GetAdCatalogProduct (string catalogId, string productId, string accountId, string? catalogAccountId = null)

Get a product

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
    public class GetAdCatalogProductExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var productId = "productId_example";  // string | Meta product item ID (from the products list; not the retailer id)
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // Get a product
                CreateAdCatalogProduct201Response result = apiInstance.GetAdCatalogProduct(catalogId, productId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.GetAdCatalogProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCatalogProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a product
    ApiResponse<CreateAdCatalogProduct201Response> response = apiInstance.GetAdCatalogProductWithHttpInfo(catalogId, productId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.GetAdCatalogProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **productId** | **string** | Meta product item ID (from the products list; not the retailer id) |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**CreateAdCatalogProduct201Response**](CreateAdCatalogProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcatalogfeeduploads"></a>
# **ListAdCatalogFeedUploads**
> ListAdCatalogFeedUploads200Response ListAdCatalogFeedUploads (string catalogId, string feedId, string accountId, string? catalogAccountId = null)

List a feed's uploads

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
    public class ListAdCatalogFeedUploadsExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var feedId = "feedId_example";  // string | 
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // List a feed's uploads
                ListAdCatalogFeedUploads200Response result = apiInstance.ListAdCatalogFeedUploads(catalogId, feedId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogFeedUploads: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCatalogFeedUploadsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List a feed's uploads
    ApiResponse<ListAdCatalogFeedUploads200Response> response = apiInstance.ListAdCatalogFeedUploadsWithHttpInfo(catalogId, feedId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogFeedUploadsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **feedId** | **string** |  |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**ListAdCatalogFeedUploads200Response**](ListAdCatalogFeedUploads200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Uploads, newest first |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcatalogfeeds"></a>
# **ListAdCatalogFeeds**
> ListAdCatalogFeeds200Response ListAdCatalogFeeds (string catalogId, string accountId, string? catalogAccountId = null)

List a catalog's product feeds

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
    public class ListAdCatalogFeedsExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // List a catalog's product feeds
                ListAdCatalogFeeds200Response result = apiInstance.ListAdCatalogFeeds(catalogId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogFeeds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCatalogFeedsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List a catalog's product feeds
    ApiResponse<ListAdCatalogFeeds200Response> response = apiInstance.ListAdCatalogFeedsWithHttpInfo(catalogId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogFeedsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**ListAdCatalogFeeds200Response**](ListAdCatalogFeeds200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Feeds |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcatalogproductsets"></a>
# **ListAdCatalogProductSets**
> ListAdCatalogProductSets200Response ListAdCatalogProductSets (string catalogId, string accountId, string? catalogAccountId = null)

List a catalog's product sets

Lists a Meta product catalog's product sets, the unit a catalog ad promotes. Pass the chosen set id, not the parent catalog id, as `promotedObject.productSetId` on POST /v1/ads/create with `goal: catalog_sales`.

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
    public class ListAdCatalogProductSetsExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 

            try
            {
                // List a catalog's product sets
                ListAdCatalogProductSets200Response result = apiInstance.ListAdCatalogProductSets(catalogId, accountId, catalogAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogProductSets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCatalogProductSetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List a catalog's product sets
    ApiResponse<ListAdCatalogProductSets200Response> response = apiInstance.ListAdCatalogProductSetsWithHttpInfo(catalogId, accountId, catalogAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogProductSetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |

### Return type

[**ListAdCatalogProductSets200Response**](ListAdCatalogProductSets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product sets |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcatalogproducts"></a>
# **ListAdCatalogProducts**
> ListAdCatalogProducts200Response ListAdCatalogProducts (string catalogId, string accountId, string? catalogAccountId = null, int? limit = null, string? after = null, string? retailerId = null)

List a catalog's products

Pages through the catalog's products. Filter by your own `retailerId` to look one up. `price` and `salePrice` come back formatted by Meta (for example \"€49.90\").

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
    public class ListAdCatalogProductsExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own (optional) 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from the previous page's `nextCursor` (optional) 
            var retailerId = "retailerId_example";  // string? | Only the product with this retailer id (your SKU) (optional) 

            try
            {
                // List a catalog's products
                ListAdCatalogProducts200Response result = apiInstance.ListAdCatalogProducts(catalogId, accountId, catalogAccountId, limit, after, retailerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCatalogProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List a catalog's products
    ApiResponse<ListAdCatalogProducts200Response> response = apiInstance.ListAdCatalogProductsWithHttpInfo(catalogId, accountId, catalogAccountId, limit, after, retailerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account&#39;s own | [optional]  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string?** | Cursor from the previous page&#39;s &#x60;nextCursor&#x60; | [optional]  |
| **retailerId** | **string?** | Only the product with this retailer id (your SKU) | [optional]  |

### Return type

[**ListAdCatalogProducts200Response**](ListAdCatalogProducts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Products |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcatalogs"></a>
# **ListAdCatalogs**
> ListAdCatalogs200Response ListAdCatalogs (string accountId, string? catalogAccountId = null, string? adAccountId = null, string? businessId = null)

List Meta product catalogs

Lists the Meta Commerce catalogs of a business portfolio (owned + agency-shared). The business comes from `businessId`, else the ad account's owner (`adAccountId`), else the WhatsApp Business Account's owner when `accountId` is a WhatsApp connection, else the only business the Meta login can see. Reads work with scopes customers already granted.

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
    public class ListAdCatalogsExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | A facebook, instagram, metaads or whatsapp account ID
            var catalogAccountId = "catalogAccountId_example";  // string? | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token is used instead of the account's own (needed for WhatsApp connections, whose token cannot manage catalogs). (optional) 
            var adAccountId = "adAccountId_example";  // string? | Meta ad account ID (act_...) whose owner business to list (optional) 
            var businessId = "businessId_example";  // string? | Meta business portfolio ID to list (optional) 

            try
            {
                // List Meta product catalogs
                ListAdCatalogs200Response result = apiInstance.ListAdCatalogs(accountId, catalogAccountId, adAccountId, businessId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCatalogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Meta product catalogs
    ApiResponse<ListAdCatalogs200Response> response = apiInstance.ListAdCatalogsWithHttpInfo(accountId, catalogAccountId, adAccountId, businessId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.ListAdCatalogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | A facebook, instagram, metaads or whatsapp account ID |  |
| **catalogAccountId** | **string?** | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token is used instead of the account&#39;s own (needed for WhatsApp connections, whose token cannot manage catalogs). | [optional]  |
| **adAccountId** | **string?** | Meta ad account ID (act_...) whose owner business to list | [optional]  |
| **businessId** | **string?** | Meta business portfolio ID to list | [optional]  |

### Return type

[**ListAdCatalogs200Response**](ListAdCatalogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **200** | Catalogs |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadcatalogproduct"></a>
# **UpdateAdCatalogProduct**
> CreateAdCatalogProduct201Response UpdateAdCatalogProduct (string catalogId, string productId, UpdateAdCatalogProductRequest updateAdCatalogProductRequest)

Update a product

Partial update: only the fields sent change. `retailerId` cannot change.

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
    public class UpdateAdCatalogProductExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var productId = "productId_example";  // string | Meta product item ID (from the products list; not the retailer id)
            var updateAdCatalogProductRequest = new UpdateAdCatalogProductRequest(); // UpdateAdCatalogProductRequest | 

            try
            {
                // Update a product
                CreateAdCatalogProduct201Response result = apiInstance.UpdateAdCatalogProduct(catalogId, productId, updateAdCatalogProductRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.UpdateAdCatalogProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdCatalogProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a product
    ApiResponse<CreateAdCatalogProduct201Response> response = apiInstance.UpdateAdCatalogProductWithHttpInfo(catalogId, productId, updateAdCatalogProductRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.UpdateAdCatalogProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **productId** | **string** | Meta product item ID (from the products list; not the retailer id) |  |
| **updateAdCatalogProductRequest** | [**UpdateAdCatalogProductRequest**](UpdateAdCatalogProductRequest.md) |  |  |

### Return type

[**CreateAdCatalogProduct201Response**](CreateAdCatalogProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadcatalogproductset"></a>
# **UpdateAdCatalogProductSet**
> CreateAdCatalogProductSet201Response UpdateAdCatalogProductSet (string catalogId, string productSetId, UpdateAdCatalogProductSetRequest updateAdCatalogProductSetRequest)

Update a product set

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
    public class UpdateAdCatalogProductSetExample
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
            var apiInstance = new ProductCatalogsApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var productSetId = "productSetId_example";  // string | 
            var updateAdCatalogProductSetRequest = new UpdateAdCatalogProductSetRequest(); // UpdateAdCatalogProductSetRequest | 

            try
            {
                // Update a product set
                CreateAdCatalogProductSet201Response result = apiInstance.UpdateAdCatalogProductSet(catalogId, productSetId, updateAdCatalogProductSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductCatalogsApi.UpdateAdCatalogProductSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdCatalogProductSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a product set
    ApiResponse<CreateAdCatalogProductSet201Response> response = apiInstance.UpdateAdCatalogProductSetWithHttpInfo(catalogId, productSetId, updateAdCatalogProductSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductCatalogsApi.UpdateAdCatalogProductSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **productSetId** | **string** |  |  |
| **updateAdCatalogProductSetRequest** | [**UpdateAdCatalogProductSetRequest**](UpdateAdCatalogProductSetRequest.md) |  |  |

### Return type

[**CreateAdCatalogProductSet201Response**](CreateAdCatalogProductSet201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product set updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login behind the account lacks catalog_management (code insufficient_permissions). Reconnect granting it, or pass catalogAccountId. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

