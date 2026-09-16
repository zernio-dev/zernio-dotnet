# Zernio.Api.ProductsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetProduct**](ProductsApi.md#getproduct) | **GET** /v1/accounts/{accountId}/products/{productId} | Get a product |
| [**ListProducts**](ProductsApi.md#listproducts) | **GET** /v1/accounts/{accountId}/products | List products |
| [**UpdateProduct**](ProductsApi.md#updateproduct) | **PATCH** /v1/accounts/{accountId}/products/{productId} | Update a product |

<a id="getproduct"></a>
# **GetProduct**
> GetProduct200Response GetProduct (string accountId, string productId)

Get a product

Fetches a single product with its variants, options and images. `productId` is the platform's numeric product id from `GET /v1/accounts/{accountId}/products`, not a Zernio id.  Supported on Shopify (platform `shopify`); accounts on other platforms return 400. 

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
    public class GetProductExample
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
            var apiInstance = new ProductsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var productId = "productId_example";  // string | Platform-native numeric product id. Non-numeric values return 400.

            try
            {
                // Get a product
                GetProduct200Response result = apiInstance.GetProduct(accountId, productId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.GetProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a product
    ApiResponse<GetProduct200Response> response = apiInstance.GetProductWithHttpInfo(accountId, productId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.GetProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **productId** | **string** | Platform-native numeric product id. Non-numeric values return 400. |  |

### Return type

[**GetProduct200Response**](GetProduct200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). The store lacks the product scopes or the token was revoked; reconnect the Shopify account. |  -  |
| **404** | Account not found or not accessible (code account_not_found), or product not found (code product_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listproducts"></a>
# **ListProducts**
> ListProducts200Response ListProducts (string accountId, int? limit = null, string? cursor = null, string? status = null, string? query = null)

List products

Lists the products on the connected store in the platform's default order, each with its variants, options and images. Cursor-paginated: pass `limit` (1-50, default 20) and the `cursor` from a previous response's `nextCursor`; `nextCursor` is null when there are no more pages. Filter with `status` and/or `query` (the platform's product search syntax, e.g. `title:*shirt* vendor:Acme tag:summer`).  Supported on Shopify (platform `shopify`); accounts on other platforms return 400. A store connected before product access was added answers 403 insufficient_permissions until the merchant reconnects it through `GET /v1/connect/shopify`. 

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
    public class ListProductsExample
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
            var apiInstance = new ProductsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var limit = 20;  // int? | Page size (1-50). (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | Opaque cursor from a previous response. Omit for the first page. (optional) 
            var status = "active";  // string? | Only products in this status. (optional) 
            var query = "query_example";  // string? | Platform product search syntax, passed through verbatim (Shopify: title, vendor, product_type, tag, sku, handle, created_at, updated_at, ...). (optional) 

            try
            {
                // List products
                ListProducts200Response result = apiInstance.ListProducts(accountId, limit, cursor, status, query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.ListProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List products
    ApiResponse<ListProducts200Response> response = apiInstance.ListProductsWithHttpInfo(accountId, limit, cursor, status, query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.ListProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **limit** | **int?** | Page size (1-50). | [optional] [default to 20] |
| **cursor** | **string?** | Opaque cursor from a previous response. Omit for the first page. | [optional]  |
| **status** | **string?** | Only products in this status. | [optional]  |
| **query** | **string?** | Platform product search syntax, passed through verbatim (Shopify: title, vendor, product_type, tag, sku, handle, created_at, updated_at, ...). | [optional]  |

### Return type

[**ListProducts200Response**](ListProducts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Products listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). The store lacks the product scopes or the token was revoked; reconnect the Shopify account. |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateproduct"></a>
# **UpdateProduct**
> GetProduct200Response UpdateProduct (string accountId, string productId, UpdateProductRequest updateProductRequest)

Update a product

Partial-updates a product. Send any subset of `title`, `descriptionHtml`, `handle`, `vendor`, `productType`, `tags`, `status`, `seo` and `variants`; at least one field is required (an empty body returns 400). `tags` replaces the full tag list. `variants` updates the price and compare-at price of the listed variant ids only; other variants are untouched, and a variant id that does not belong to the product is a 400. Responds with the product as it is after the update.  Supported on Shopify (platform `shopify`); accounts on other platforms return 400. A store connected before product access was added answers 403 insufficient_permissions until the merchant reconnects it through `GET /v1/connect/shopify`. 

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
    public class UpdateProductExample
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
            var apiInstance = new ProductsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected Shopify SocialAccount id.
            var productId = "productId_example";  // string | Platform-native numeric product id. Non-numeric values return 400.
            var updateProductRequest = new UpdateProductRequest(); // UpdateProductRequest | 

            try
            {
                // Update a product
                GetProduct200Response result = apiInstance.UpdateProduct(accountId, productId, updateProductRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.UpdateProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a product
    ApiResponse<GetProduct200Response> response = apiInstance.UpdateProductWithHttpInfo(accountId, productId, updateProductRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.UpdateProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected Shopify SocialAccount id. |  |
| **productId** | **string** | Platform-native numeric product id. Non-numeric values return 400. |  |
| **updateProductRequest** | [**UpdateProductRequest**](UpdateProductRequest.md) |  |  |

### Return type

[**GetProduct200Response**](GetProduct200Response.md)

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
| **403** | The platform rejected the request (code insufficient_permissions). The store lacks the product scopes or the token was revoked; reconnect the Shopify account. |  -  |
| **404** | Account not found or not accessible (code account_not_found), or product not found (code product_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by Shopify. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

