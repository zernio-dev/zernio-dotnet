# Zernio.Api.CommerceApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddCommerceDiscountCodes**](CommerceApi.md#addcommercediscountcodes) | **POST** /v1/commerce/discounts/{discountId}/codes | Add codes to a discount |
| [**AddCommerceMarketingEngagement**](CommerceApi.md#addcommercemarketingengagement) | **POST** /v1/commerce/marketing-activities/{remoteId}/engagements | Report daily engagement |
| [**AddCommerceProductImages**](CommerceApi.md#addcommerceproductimages) | **POST** /v1/commerce/products/{productId}/images | Add images |
| [**ChangeCollectionChannels**](CommerceApi.md#changecollectionchannels) | **POST** /v1/commerce/collections/{collectionId}/channels | Publish or unpublish a collection |
| [**ChangeCommerceCollectionProducts**](CommerceApi.md#changecommercecollectionproducts) | **POST** /v1/commerce/collections/{collectionId}/products | Add or remove products in a collection |
| [**ChangeCommerceInventory**](CommerceApi.md#changecommerceinventory) | **POST** /v1/commerce/products/{productId}/inventory | Set or adjust stock |
| [**ChangeCommerceProductState**](CommerceApi.md#changecommerceproductstate) | **POST** /v1/commerce/products/state | Activate, deactivate, archive or delete products |
| [**ChangeCommerceProductTags**](CommerceApi.md#changecommerceproducttags) | **POST** /v1/commerce/products/tags | Add or remove tags in bulk |
| [**ChangeProductChannels**](CommerceApi.md#changeproductchannels) | **POST** /v1/commerce/products/{productId}/channels | Publish or unpublish a product |
| [**CreateCommerceCatalogSync**](CommerceApi.md#createcommercecatalogsync) | **POST** /v1/commerce/catalog-syncs | Sync a store into a Meta catalog |
| [**CreateCommerceCollection**](CommerceApi.md#createcommercecollection) | **POST** /v1/commerce/collections | Create a collection |
| [**CreateCommerceDiscount**](CommerceApi.md#createcommercediscount) | **POST** /v1/commerce/discounts | Create a discount |
| [**CreateCommerceMenu**](CommerceApi.md#createcommercemenu) | **POST** /v1/commerce/menus | Create a navigation menu |
| [**CreateCommerceMetaobject**](CommerceApi.md#createcommercemetaobject) | **POST** /v1/commerce/metaobjects | Create a metaobject |
| [**CreateCommercePage**](CommerceApi.md#createcommercepage) | **POST** /v1/commerce/pages | Create a page |
| [**CreateCommerceProduct**](CommerceApi.md#createcommerceproduct) | **POST** /v1/commerce/products | Create a product |
| [**CreateCommerceProductOptions**](CommerceApi.md#createcommerceproductoptions) | **POST** /v1/commerce/products/{productId}/options | Add options |
| [**CreateCommerceProductVariants**](CommerceApi.md#createcommerceproductvariants) | **POST** /v1/commerce/products/{productId}/variants | Add variants |
| [**CreateCommerceRedirect**](CommerceApi.md#createcommerceredirect) | **POST** /v1/commerce/redirects | Create a URL redirect |
| [**DeleteCollectionMetafields**](CommerceApi.md#deletecollectionmetafields) | **DELETE** /v1/commerce/collections/{collectionId}/metafields | Delete collection metafields |
| [**DeleteCommerceCatalogSync**](CommerceApi.md#deletecommercecatalogsync) | **DELETE** /v1/commerce/catalog-syncs/{syncId} | Stop a catalog sync |
| [**DeleteCommerceCollection**](CommerceApi.md#deletecommercecollection) | **DELETE** /v1/commerce/collections/{collectionId} | Delete a collection |
| [**DeleteCommerceDiscount**](CommerceApi.md#deletecommercediscount) | **DELETE** /v1/commerce/discounts/{discountId} | Delete a discount |
| [**DeleteCommerceMarketingActivity**](CommerceApi.md#deletecommercemarketingactivity) | **DELETE** /v1/commerce/marketing-activities/{remoteId} | Delete a marketing activity |
| [**DeleteCommerceMenu**](CommerceApi.md#deletecommercemenu) | **DELETE** /v1/commerce/menus/{menuId} | Delete a navigation menu |
| [**DeleteCommerceMetaobject**](CommerceApi.md#deletecommercemetaobject) | **DELETE** /v1/commerce/metaobjects/{metaobjectId} | Delete a metaobject |
| [**DeleteCommercePage**](CommerceApi.md#deletecommercepage) | **DELETE** /v1/commerce/pages/{pageId} | Delete a page |
| [**DeleteCommercePriceListPrices**](CommerceApi.md#deletecommercepricelistprices) | **DELETE** /v1/commerce/price-lists/{priceListId}/prices | Remove fixed prices |
| [**DeleteCommerceProductOptions**](CommerceApi.md#deletecommerceproductoptions) | **DELETE** /v1/commerce/products/{productId}/options | Delete options |
| [**DeleteCommerceProductVariants**](CommerceApi.md#deletecommerceproductvariants) | **DELETE** /v1/commerce/products/{productId}/variants | Delete variants |
| [**DeleteCommerceRedirect**](CommerceApi.md#deletecommerceredirect) | **DELETE** /v1/commerce/redirects/{redirectId} | Delete a URL redirect |
| [**DeleteProductMetafields**](CommerceApi.md#deleteproductmetafields) | **DELETE** /v1/commerce/products/{productId}/metafields | Delete product metafields |
| [**DuplicateCommerceProduct**](CommerceApi.md#duplicatecommerceproduct) | **POST** /v1/commerce/products/{productId}/duplicate | Duplicate a product |
| [**GetCommerceCatalogSync**](CommerceApi.md#getcommercecatalogsync) | **GET** /v1/commerce/catalog-syncs/{syncId} | Get a catalog sync |
| [**GetCommerceCollection**](CommerceApi.md#getcommercecollection) | **GET** /v1/commerce/collections/{collectionId} | Get a collection |
| [**GetCommerceDiscount**](CommerceApi.md#getcommercediscount) | **GET** /v1/commerce/discounts/{discountId} | Get a discount |
| [**GetCommerceMenu**](CommerceApi.md#getcommercemenu) | **GET** /v1/commerce/menus/{menuId} | Get a navigation menu |
| [**GetCommerceMetaobject**](CommerceApi.md#getcommercemetaobject) | **GET** /v1/commerce/metaobjects/{metaobjectId} | Get a metaobject |
| [**GetCommercePage**](CommerceApi.md#getcommercepage) | **GET** /v1/commerce/pages/{pageId} | Get a page |
| [**GetCommerceProduct**](CommerceApi.md#getcommerceproduct) | **GET** /v1/commerce/products/{productId} | Get a product |
| [**GetCommerceStore**](CommerceApi.md#getcommercestore) | **GET** /v1/commerce/store | Get a store |
| [**ListCollectionMetafields**](CommerceApi.md#listcollectionmetafields) | **GET** /v1/commerce/collections/{collectionId}/metafields | List collection metafields |
| [**ListCommerceCatalogSyncs**](CommerceApi.md#listcommercecatalogsyncs) | **GET** /v1/commerce/catalog-syncs | List catalog syncs |
| [**ListCommerceChannels**](CommerceApi.md#listcommercechannels) | **GET** /v1/commerce/channels | List sales channels |
| [**ListCommerceCollections**](CommerceApi.md#listcommercecollections) | **GET** /v1/commerce/collections | List collections |
| [**ListCommerceDiscounts**](CommerceApi.md#listcommercediscounts) | **GET** /v1/commerce/discounts | List discounts |
| [**ListCommerceInventory**](CommerceApi.md#listcommerceinventory) | **GET** /v1/commerce/inventory | Get a product&#39;s stock |
| [**ListCommerceLocations**](CommerceApi.md#listcommercelocations) | **GET** /v1/commerce/locations | List locations |
| [**ListCommerceMarkets**](CommerceApi.md#listcommercemarkets) | **GET** /v1/commerce/markets | List markets |
| [**ListCommerceMenus**](CommerceApi.md#listcommercemenus) | **GET** /v1/commerce/menus | List navigation menus |
| [**ListCommerceMetaobjectDefinitions**](CommerceApi.md#listcommercemetaobjectdefinitions) | **GET** /v1/commerce/metaobject-definitions | List metaobject definitions |
| [**ListCommerceMetaobjects**](CommerceApi.md#listcommercemetaobjects) | **GET** /v1/commerce/metaobjects | List metaobjects of a type |
| [**ListCommercePages**](CommerceApi.md#listcommercepages) | **GET** /v1/commerce/pages | List pages |
| [**ListCommercePriceLists**](CommerceApi.md#listcommercepricelists) | **GET** /v1/commerce/price-lists | List price lists |
| [**ListCommerceProducts**](CommerceApi.md#listcommerceproducts) | **GET** /v1/commerce/products | List products |
| [**ListCommerceRedirects**](CommerceApi.md#listcommerceredirects) | **GET** /v1/commerce/redirects | List URL redirects |
| [**ListProductMetafields**](CommerceApi.md#listproductmetafields) | **GET** /v1/commerce/products/{productId}/metafields | List product metafields |
| [**RemoveCommerceProductImages**](CommerceApi.md#removecommerceproductimages) | **DELETE** /v1/commerce/products/{productId}/images | Remove images |
| [**ReorderCommerceCollectionProducts**](CommerceApi.md#reordercommercecollectionproducts) | **POST** /v1/commerce/collections/{collectionId}/reorder | Reorder products in a collection |
| [**ReorderCommerceProductImages**](CommerceApi.md#reordercommerceproductimages) | **POST** /v1/commerce/products/{productId}/images/reorder | Reorder images |
| [**RunCommerceCatalogSync**](CommerceApi.md#runcommercecatalogsync) | **POST** /v1/commerce/catalog-syncs/{syncId}/run | Run a catalog sync now |
| [**SetCollectionMetafields**](CommerceApi.md#setcollectionmetafields) | **PUT** /v1/commerce/collections/{collectionId}/metafields | Set collection metafields |
| [**SetCommerceDiscountActive**](CommerceApi.md#setcommercediscountactive) | **POST** /v1/commerce/discounts/{discountId}/state | Activate or deactivate a discount |
| [**SetCommercePriceListPrices**](CommerceApi.md#setcommercepricelistprices) | **PUT** /v1/commerce/price-lists/{priceListId}/prices | Set fixed prices |
| [**SetProductMetafields**](CommerceApi.md#setproductmetafields) | **PUT** /v1/commerce/products/{productId}/metafields | Set product metafields |
| [**UpdateCommerceCollection**](CommerceApi.md#updatecommercecollection) | **PATCH** /v1/commerce/collections/{collectionId} | Update a collection |
| [**UpdateCommerceDiscount**](CommerceApi.md#updatecommercediscount) | **PATCH** /v1/commerce/discounts/{discountId} | Update a discount |
| [**UpdateCommerceMenu**](CommerceApi.md#updatecommercemenu) | **PUT** /v1/commerce/menus/{menuId} | Replace a navigation menu |
| [**UpdateCommerceMetaobject**](CommerceApi.md#updatecommercemetaobject) | **PATCH** /v1/commerce/metaobjects/{metaobjectId} | Update a metaobject |
| [**UpdateCommercePage**](CommerceApi.md#updatecommercepage) | **PATCH** /v1/commerce/pages/{pageId} | Update a page |
| [**UpdateCommerceProduct**](CommerceApi.md#updatecommerceproduct) | **PATCH** /v1/commerce/products/{productId} | Update a product |
| [**UpdateCommerceProductPrices**](CommerceApi.md#updatecommerceproductprices) | **POST** /v1/commerce/products/{productId}/price | Update variant prices |
| [**UpdateCommerceRedirect**](CommerceApi.md#updatecommerceredirect) | **PATCH** /v1/commerce/redirects/{redirectId} | Update a URL redirect |
| [**UpsertCommerceMarketingActivity**](CommerceApi.md#upsertcommercemarketingactivity) | **PUT** /v1/commerce/marketing-activities | Record a marketing activity |

<a id="addcommercediscountcodes"></a>
# **AddCommerceDiscountCodes**
> ReorderCommerceProductImages200Response AddCommerceDiscountCodes (string discountId, AddCommerceDiscountCodesRequest addCommerceDiscountCodesRequest)

Add codes to a discount

Adds up to 250 more codes to a code discount, for example one per influencer. The platform adds them in the background. 

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
    public class AddCommerceDiscountCodesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var discountId = "discountId_example";  // string | Platform-native id.
            var addCommerceDiscountCodesRequest = new AddCommerceDiscountCodesRequest(); // AddCommerceDiscountCodesRequest | 

            try
            {
                // Add codes to a discount
                ReorderCommerceProductImages200Response result = apiInstance.AddCommerceDiscountCodes(discountId, addCommerceDiscountCodesRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.AddCommerceDiscountCodes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddCommerceDiscountCodesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add codes to a discount
    ApiResponse<ReorderCommerceProductImages200Response> response = apiInstance.AddCommerceDiscountCodesWithHttpInfo(discountId, addCommerceDiscountCodesRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.AddCommerceDiscountCodesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **discountId** | **string** | Platform-native id. |  |
| **addCommerceDiscountCodesRequest** | [**AddCommerceDiscountCodesRequest**](AddCommerceDiscountCodesRequest.md) |  |  |

### Return type

[**ReorderCommerceProductImages200Response**](ReorderCommerceProductImages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Codes queued |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addcommercemarketingengagement"></a>
# **AddCommerceMarketingEngagement**
> AddCommerceMarketingEngagement201Response AddCommerceMarketingEngagement (string remoteId, AddCommerceMarketingEngagementRequest addCommerceMarketingEngagementRequest)

Report daily engagement

Reports one day's numbers for an activity (UTC day), shown next to it in the store's Marketing section. 

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
    public class AddCommerceMarketingEngagementExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var remoteId = "remoteId_example";  // string | The remoteId given when recording it.
            var addCommerceMarketingEngagementRequest = new AddCommerceMarketingEngagementRequest(); // AddCommerceMarketingEngagementRequest | 

            try
            {
                // Report daily engagement
                AddCommerceMarketingEngagement201Response result = apiInstance.AddCommerceMarketingEngagement(remoteId, addCommerceMarketingEngagementRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.AddCommerceMarketingEngagement: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddCommerceMarketingEngagementWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Report daily engagement
    ApiResponse<AddCommerceMarketingEngagement201Response> response = apiInstance.AddCommerceMarketingEngagementWithHttpInfo(remoteId, addCommerceMarketingEngagementRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.AddCommerceMarketingEngagementWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **remoteId** | **string** | The remoteId given when recording it. |  |
| **addCommerceMarketingEngagementRequest** | [**AddCommerceMarketingEngagementRequest**](AddCommerceMarketingEngagementRequest.md) |  |  |

### Return type

[**AddCommerceMarketingEngagement201Response**](AddCommerceMarketingEngagement201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Engagement recorded |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="addcommerceproductimages"></a>
# **AddCommerceProductImages**
> CreateCommerceProduct201Response AddCommerceProductImages (string productId, AddCommerceProductImagesRequest addCommerceProductImagesRequest)

Add images

Adds images from public URLs. The platform fetches them, so they can appear on the product a few seconds after the call returns. 

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
    public class AddCommerceProductImagesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var addCommerceProductImagesRequest = new AddCommerceProductImagesRequest(); // AddCommerceProductImagesRequest | 

            try
            {
                // Add images
                CreateCommerceProduct201Response result = apiInstance.AddCommerceProductImages(productId, addCommerceProductImagesRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.AddCommerceProductImages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddCommerceProductImagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add images
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.AddCommerceProductImagesWithHttpInfo(productId, addCommerceProductImagesRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.AddCommerceProductImagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **addCommerceProductImagesRequest** | [**AddCommerceProductImagesRequest**](AddCommerceProductImagesRequest.md) |  |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="changecollectionchannels"></a>
# **ChangeCollectionChannels**
> ChangeCollectionChannels200Response ChangeCollectionChannels (string collectionId, ChangeProductChannelsRequest changeProductChannelsRequest)

Publish or unpublish a collection

Publishes to and/or unpublishes from sales channels (the online store, Shop, POS and others). List channels with GET /v1/commerce/channels. 

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
    public class ChangeCollectionChannelsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native id.
            var changeProductChannelsRequest = new ChangeProductChannelsRequest(); // ChangeProductChannelsRequest | 

            try
            {
                // Publish or unpublish a collection
                ChangeCollectionChannels200Response result = apiInstance.ChangeCollectionChannels(collectionId, changeProductChannelsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ChangeCollectionChannels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChangeCollectionChannelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Publish or unpublish a collection
    ApiResponse<ChangeCollectionChannels200Response> response = apiInstance.ChangeCollectionChannelsWithHttpInfo(collectionId, changeProductChannelsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ChangeCollectionChannelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native id. |  |
| **changeProductChannelsRequest** | [**ChangeProductChannelsRequest**](ChangeProductChannelsRequest.md) |  |  |

### Return type

[**ChangeCollectionChannels200Response**](ChangeCollectionChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Publication changed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="changecommercecollectionproducts"></a>
# **ChangeCommerceCollectionProducts**
> ChangeCommerceCollectionProducts200Response ChangeCommerceCollectionProducts (string collectionId, ChangeCommerceCollectionProductsRequest changeCommerceCollectionProductsRequest)

Add or remove products in a collection

Adds and/or removes hand-picked products. Products a collection includes through its own rules are not affected. `pending` is true when the platform finishes the change in the background; the product count then catches up a few seconds later. 

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
    public class ChangeCommerceCollectionProductsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native collection id.
            var changeCommerceCollectionProductsRequest = new ChangeCommerceCollectionProductsRequest(); // ChangeCommerceCollectionProductsRequest | 

            try
            {
                // Add or remove products in a collection
                ChangeCommerceCollectionProducts200Response result = apiInstance.ChangeCommerceCollectionProducts(collectionId, changeCommerceCollectionProductsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ChangeCommerceCollectionProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChangeCommerceCollectionProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add or remove products in a collection
    ApiResponse<ChangeCommerceCollectionProducts200Response> response = apiInstance.ChangeCommerceCollectionProductsWithHttpInfo(collectionId, changeCommerceCollectionProductsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ChangeCommerceCollectionProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native collection id. |  |
| **changeCommerceCollectionProductsRequest** | [**ChangeCommerceCollectionProductsRequest**](ChangeCommerceCollectionProductsRequest.md) |  |  |

### Return type

[**ChangeCommerceCollectionProducts200Response**](ChangeCommerceCollectionProducts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Membership changed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found (code account_not_found) or collection not found (code resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="changecommerceinventory"></a>
# **ChangeCommerceInventory**
> ListCommerceInventory200Response ChangeCommerceInventory (string productId, ChangeCommerceInventoryRequest changeCommerceInventoryRequest)

Set or adjust stock

`set` makes `quantity` the new available count; `adjust` adds `quantity` (negative to subtract). The variant must be stocked at the location. Answers the product's stock after the change. 

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
    public class ChangeCommerceInventoryExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var changeCommerceInventoryRequest = new ChangeCommerceInventoryRequest(); // ChangeCommerceInventoryRequest | 

            try
            {
                // Set or adjust stock
                ListCommerceInventory200Response result = apiInstance.ChangeCommerceInventory(productId, changeCommerceInventoryRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ChangeCommerceInventory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChangeCommerceInventoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set or adjust stock
    ApiResponse<ListCommerceInventory200Response> response = apiInstance.ChangeCommerceInventoryWithHttpInfo(productId, changeCommerceInventoryRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ChangeCommerceInventoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **changeCommerceInventoryRequest** | [**ChangeCommerceInventoryRequest**](ChangeCommerceInventoryRequest.md) |  |  |

### Return type

[**ListCommerceInventory200Response**](ListCommerceInventory200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stock changed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="changecommerceproductstate"></a>
# **ChangeCommerceProductState**
> ChangeCommerceProductState200Response ChangeCommerceProductState (ChangeCommerceProductStateRequest changeCommerceProductStateRequest)

Activate, deactivate, archive or delete products

Applies one action to up to 50 products and reports each product's outcome, so one failure does not abort the rest. On Shopify, `deactivate` sets the product to draft and `delete` is permanent. 

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
    public class ChangeCommerceProductStateExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var changeCommerceProductStateRequest = new ChangeCommerceProductStateRequest(); // ChangeCommerceProductStateRequest | 

            try
            {
                // Activate, deactivate, archive or delete products
                ChangeCommerceProductState200Response result = apiInstance.ChangeCommerceProductState(changeCommerceProductStateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ChangeCommerceProductState: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChangeCommerceProductStateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Activate, deactivate, archive or delete products
    ApiResponse<ChangeCommerceProductState200Response> response = apiInstance.ChangeCommerceProductStateWithHttpInfo(changeCommerceProductStateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ChangeCommerceProductStateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **changeCommerceProductStateRequest** | [**ChangeCommerceProductStateRequest**](ChangeCommerceProductStateRequest.md) |  |  |

### Return type

[**ChangeCommerceProductState200Response**](ChangeCommerceProductState200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Action applied |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="changecommerceproducttags"></a>
# **ChangeCommerceProductTags**
> ChangeCommerceProductTags200Response ChangeCommerceProductTags (ChangeCommerceProductTagsRequest changeCommerceProductTagsRequest)

Add or remove tags in bulk

Adds and/or removes tags on up to 50 products and reports each product's outcome. 

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
    public class ChangeCommerceProductTagsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var changeCommerceProductTagsRequest = new ChangeCommerceProductTagsRequest(); // ChangeCommerceProductTagsRequest | 

            try
            {
                // Add or remove tags in bulk
                ChangeCommerceProductTags200Response result = apiInstance.ChangeCommerceProductTags(changeCommerceProductTagsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ChangeCommerceProductTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChangeCommerceProductTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add or remove tags in bulk
    ApiResponse<ChangeCommerceProductTags200Response> response = apiInstance.ChangeCommerceProductTagsWithHttpInfo(changeCommerceProductTagsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ChangeCommerceProductTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **changeCommerceProductTagsRequest** | [**ChangeCommerceProductTagsRequest**](ChangeCommerceProductTagsRequest.md) |  |  |

### Return type

[**ChangeCommerceProductTags200Response**](ChangeCommerceProductTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tags changed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="changeproductchannels"></a>
# **ChangeProductChannels**
> ChangeProductChannels200Response ChangeProductChannels (string productId, ChangeProductChannelsRequest changeProductChannelsRequest)

Publish or unpublish a product

Publishes to and/or unpublishes from sales channels (the online store, Shop, POS and others). List channels with GET /v1/commerce/channels. 

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
    public class ChangeProductChannelsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var changeProductChannelsRequest = new ChangeProductChannelsRequest(); // ChangeProductChannelsRequest | 

            try
            {
                // Publish or unpublish a product
                ChangeProductChannels200Response result = apiInstance.ChangeProductChannels(productId, changeProductChannelsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ChangeProductChannels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChangeProductChannelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Publish or unpublish a product
    ApiResponse<ChangeProductChannels200Response> response = apiInstance.ChangeProductChannelsWithHttpInfo(productId, changeProductChannelsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ChangeProductChannelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **changeProductChannelsRequest** | [**ChangeProductChannelsRequest**](ChangeProductChannelsRequest.md) |  |  |

### Return type

[**ChangeProductChannels200Response**](ChangeProductChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Publication changed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommercecatalogsync"></a>
# **CreateCommerceCatalogSync**
> CreateCommerceCatalogSync202Response CreateCommerceCatalogSync (CreateCommerceCatalogSyncRequest createCommerceCatalogSyncRequest)

Sync a store into a Meta catalog

Keeps a Meta product catalog in sync with the store, for catalog ads (`goal: catalog_sales`) and Shops. The first full run starts right away in the background; `runStatus` and the item counts report its outcome. Every active product variant that is published to the online store and has an image becomes a catalog item, grouped by product (`item_group_id`). After that, product changes on the store update the catalog within minutes, and a daily full run removes items for products or variants the store no longer has. Items are namespaced to the store, so a catalog can take several stores and a run never touches items it did not create.  `catalogAccountId` is a connected facebook, instagram or metaads account whose Meta login can manage the catalog (the catalog_management permission); find catalogs with `GET /v1/ads/catalogs`. 

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
    public class CreateCommerceCatalogSyncExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommerceCatalogSyncRequest = new CreateCommerceCatalogSyncRequest(); // CreateCommerceCatalogSyncRequest | 

            try
            {
                // Sync a store into a Meta catalog
                CreateCommerceCatalogSync202Response result = apiInstance.CreateCommerceCatalogSync(createCommerceCatalogSyncRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceCatalogSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceCatalogSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sync a store into a Meta catalog
    ApiResponse<CreateCommerceCatalogSync202Response> response = apiInstance.CreateCommerceCatalogSyncWithHttpInfo(createCommerceCatalogSyncRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceCatalogSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommerceCatalogSyncRequest** | [**CreateCommerceCatalogSyncRequest**](CreateCommerceCatalogSyncRequest.md) |  |  |

### Return type

[**CreateCommerceCatalogSync202Response**](CreateCommerceCatalogSync202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Sync created; the first run is queued |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The Meta login cannot manage the catalog (code insufficient_permissions). |  -  |
| **404** | Account or catalog not found (code account_not_found or resource_not_found). |  -  |
| **409** | The store already syncs to that catalog (code catalog_sync_conflict). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommercecollection"></a>
# **CreateCommerceCollection**
> CreateCommerceCollection201Response CreateCommerceCollection (CreateCommerceCollectionRequest createCommerceCollectionRequest)

Create a collection

Creates a collection, optionally with hand-picked products. On Shopify the collection starts unpublished from the online store; publish it from the Shopify admin. 

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
    public class CreateCommerceCollectionExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommerceCollectionRequest = new CreateCommerceCollectionRequest(); // CreateCommerceCollectionRequest | 

            try
            {
                // Create a collection
                CreateCommerceCollection201Response result = apiInstance.CreateCommerceCollection(createCommerceCollectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceCollection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceCollectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a collection
    ApiResponse<CreateCommerceCollection201Response> response = apiInstance.CreateCommerceCollectionWithHttpInfo(createCommerceCollectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceCollectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommerceCollectionRequest** | [**CreateCommerceCollectionRequest**](CreateCommerceCollectionRequest.md) |  |  |

### Return type

[**CreateCommerceCollection201Response**](CreateCommerceCollection201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Collection created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found (code account_not_found) or collection not found (code resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommercediscount"></a>
# **CreateCommerceDiscount**
> CreateCommerceDiscount201Response CreateCommerceDiscount (CreateCommerceDiscountRequest createCommerceDiscountRequest)

Create a discount

Creates a code discount (buyers enter a code) or an automatic one (applied at checkout), as a percentage, a fixed amount or free shipping. It applies to every product unless productIds or collectionIds narrow it, and to every buyer. 

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
    public class CreateCommerceDiscountExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommerceDiscountRequest = new CreateCommerceDiscountRequest(); // CreateCommerceDiscountRequest | 

            try
            {
                // Create a discount
                CreateCommerceDiscount201Response result = apiInstance.CreateCommerceDiscount(createCommerceDiscountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceDiscount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceDiscountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a discount
    ApiResponse<CreateCommerceDiscount201Response> response = apiInstance.CreateCommerceDiscountWithHttpInfo(createCommerceDiscountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceDiscountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommerceDiscountRequest** | [**CreateCommerceDiscountRequest**](CreateCommerceDiscountRequest.md) |  |  |

### Return type

[**CreateCommerceDiscount201Response**](CreateCommerceDiscount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Discount created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommercemenu"></a>
# **CreateCommerceMenu**
> CreateCommerceMenu201Response CreateCommerceMenu (CreateCommerceMenuRequest createCommerceMenuRequest)

Create a navigation menu

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
    public class CreateCommerceMenuExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommerceMenuRequest = new CreateCommerceMenuRequest(); // CreateCommerceMenuRequest | 

            try
            {
                // Create a navigation menu
                CreateCommerceMenu201Response result = apiInstance.CreateCommerceMenu(createCommerceMenuRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceMenu: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceMenuWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a navigation menu
    ApiResponse<CreateCommerceMenu201Response> response = apiInstance.CreateCommerceMenuWithHttpInfo(createCommerceMenuRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceMenuWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommerceMenuRequest** | [**CreateCommerceMenuRequest**](CreateCommerceMenuRequest.md) |  |  |

### Return type

[**CreateCommerceMenu201Response**](CreateCommerceMenu201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Menu created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommercemetaobject"></a>
# **CreateCommerceMetaobject**
> CreateCommerceMetaobject201Response CreateCommerceMetaobject (CreateCommerceMetaobjectRequest createCommerceMetaobjectRequest)

Create a metaobject

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
    public class CreateCommerceMetaobjectExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommerceMetaobjectRequest = new CreateCommerceMetaobjectRequest(); // CreateCommerceMetaobjectRequest | 

            try
            {
                // Create a metaobject
                CreateCommerceMetaobject201Response result = apiInstance.CreateCommerceMetaobject(createCommerceMetaobjectRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceMetaobject: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceMetaobjectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a metaobject
    ApiResponse<CreateCommerceMetaobject201Response> response = apiInstance.CreateCommerceMetaobjectWithHttpInfo(createCommerceMetaobjectRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceMetaobjectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommerceMetaobjectRequest** | [**CreateCommerceMetaobjectRequest**](CreateCommerceMetaobjectRequest.md) |  |  |

### Return type

[**CreateCommerceMetaobject201Response**](CreateCommerceMetaobject201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Metaobject created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommercepage"></a>
# **CreateCommercePage**
> CreateCommercePage201Response CreateCommercePage (CreateCommercePageRequest createCommercePageRequest)

Create a page

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
    public class CreateCommercePageExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommercePageRequest = new CreateCommercePageRequest(); // CreateCommercePageRequest | 

            try
            {
                // Create a page
                CreateCommercePage201Response result = apiInstance.CreateCommercePage(createCommercePageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommercePage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommercePageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a page
    ApiResponse<CreateCommercePage201Response> response = apiInstance.CreateCommercePageWithHttpInfo(createCommercePageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommercePageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommercePageRequest** | [**CreateCommercePageRequest**](CreateCommercePageRequest.md) |  |  |

### Return type

[**CreateCommercePage201Response**](CreateCommercePage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Page created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommerceproduct"></a>
# **CreateCommerceProduct**
> CreateCommerceProduct201Response CreateCommerceProduct (CreateCommerceProductRequest createCommerceProductRequest)

Create a product

Creates a product with its options and variants. `status` defaults to `draft`: no platform offers a sandbox for product writes, so nothing goes on sale unless you ask for `active`. A product without `options` has exactly one variant. Images are fetched by the platform from the given URLs and may appear on the product a few seconds later. 

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
    public class CreateCommerceProductExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommerceProductRequest = new CreateCommerceProductRequest(); // CreateCommerceProductRequest | 

            try
            {
                // Create a product
                CreateCommerceProduct201Response result = apiInstance.CreateCommerceProduct(createCommerceProductRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a product
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.CreateCommerceProductWithHttpInfo(createCommerceProductRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommerceProductRequest** | [**CreateCommerceProductRequest**](CreateCommerceProductRequest.md) |  |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

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
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommerceproductoptions"></a>
# **CreateCommerceProductOptions**
> CreateCommerceProduct201Response CreateCommerceProductOptions (string productId, CreateCommerceProductOptionsRequest createCommerceProductOptionsRequest)

Add options

Adds option axes (e.g. Size, Color) and their values. With createVariants true the platform creates a variant for every new combination; otherwise existing variants take the first value. 

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
    public class CreateCommerceProductOptionsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var createCommerceProductOptionsRequest = new CreateCommerceProductOptionsRequest(); // CreateCommerceProductOptionsRequest | 

            try
            {
                // Add options
                CreateCommerceProduct201Response result = apiInstance.CreateCommerceProductOptions(productId, createCommerceProductOptionsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceProductOptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceProductOptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add options
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.CreateCommerceProductOptionsWithHttpInfo(productId, createCommerceProductOptionsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceProductOptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **createCommerceProductOptionsRequest** | [**CreateCommerceProductOptionsRequest**](CreateCommerceProductOptionsRequest.md) |  |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommerceproductvariants"></a>
# **CreateCommerceProductVariants**
> CreateCommerceProduct201Response CreateCommerceProductVariants (string productId, CreateCommerceProductVariantsRequest createCommerceProductVariantsRequest)

Add variants

Adds variants to a product. Each variant names a value for every product option (create options first with POST .../options). A product's placeholder default variant is replaced when real ones arrive. 

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
    public class CreateCommerceProductVariantsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var createCommerceProductVariantsRequest = new CreateCommerceProductVariantsRequest(); // CreateCommerceProductVariantsRequest | 

            try
            {
                // Add variants
                CreateCommerceProduct201Response result = apiInstance.CreateCommerceProductVariants(productId, createCommerceProductVariantsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceProductVariants: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceProductVariantsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add variants
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.CreateCommerceProductVariantsWithHttpInfo(productId, createCommerceProductVariantsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceProductVariantsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **createCommerceProductVariantsRequest** | [**CreateCommerceProductVariantsRequest**](CreateCommerceProductVariantsRequest.md) |  |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createcommerceredirect"></a>
# **CreateCommerceRedirect**
> CreateCommerceRedirect201Response CreateCommerceRedirect (CreateCommerceRedirectRequest createCommerceRedirectRequest)

Create a URL redirect

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
    public class CreateCommerceRedirectExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var createCommerceRedirectRequest = new CreateCommerceRedirectRequest(); // CreateCommerceRedirectRequest | 

            try
            {
                // Create a URL redirect
                CreateCommerceRedirect201Response result = apiInstance.CreateCommerceRedirect(createCommerceRedirectRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.CreateCommerceRedirect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCommerceRedirectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a URL redirect
    ApiResponse<CreateCommerceRedirect201Response> response = apiInstance.CreateCommerceRedirectWithHttpInfo(createCommerceRedirectRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.CreateCommerceRedirectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCommerceRedirectRequest** | [**CreateCommerceRedirectRequest**](CreateCommerceRedirectRequest.md) |  |  |

### Return type

[**CreateCommerceRedirect201Response**](CreateCommerceRedirect201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Redirect created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecollectionmetafields"></a>
# **DeleteCollectionMetafields**
> DeleteProductMetafields200Response DeleteCollectionMetafields (string collectionId, string accountId, string keys)

Delete collection metafields

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
    public class DeleteCollectionMetafieldsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var keys = "keys_example";  // string | Comma-separated namespace.key pairs.

            try
            {
                // Delete collection metafields
                DeleteProductMetafields200Response result = apiInstance.DeleteCollectionMetafields(collectionId, accountId, keys);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCollectionMetafields: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCollectionMetafieldsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete collection metafields
    ApiResponse<DeleteProductMetafields200Response> response = apiInstance.DeleteCollectionMetafieldsWithHttpInfo(collectionId, accountId, keys);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCollectionMetafieldsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **keys** | **string** | Comma-separated namespace.key pairs. |  |

### Return type

[**DeleteProductMetafields200Response**](DeleteProductMetafields200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metafields deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercecatalogsync"></a>
# **DeleteCommerceCatalogSync**
> DeleteCommerceCatalogSync200Response DeleteCommerceCatalogSync (string syncId)

Stop a catalog sync

Stops syncing. Items already in the catalog stay there.

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
    public class DeleteCommerceCatalogSyncExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var syncId = "syncId_example";  // string | 

            try
            {
                // Stop a catalog sync
                DeleteCommerceCatalogSync200Response result = apiInstance.DeleteCommerceCatalogSync(syncId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceCatalogSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceCatalogSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Stop a catalog sync
    ApiResponse<DeleteCommerceCatalogSync200Response> response = apiInstance.DeleteCommerceCatalogSyncWithHttpInfo(syncId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceCatalogSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **syncId** | **string** |  |  |

### Return type

[**DeleteCommerceCatalogSync200Response**](DeleteCommerceCatalogSync200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog sync stopped |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Catalog sync not found (code resource_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercecollection"></a>
# **DeleteCommerceCollection**
> DeleteCommerceCollection200Response DeleteCommerceCollection (string collectionId, string accountId)

Delete a collection

Deletes the collection. Its products are not affected.

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
    public class DeleteCommerceCollectionExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native collection id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Delete a collection
                DeleteCommerceCollection200Response result = apiInstance.DeleteCommerceCollection(collectionId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceCollection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceCollectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a collection
    ApiResponse<DeleteCommerceCollection200Response> response = apiInstance.DeleteCommerceCollectionWithHttpInfo(collectionId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceCollectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native collection id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**DeleteCommerceCollection200Response**](DeleteCommerceCollection200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collection deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found (code account_not_found) or collection not found (code resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercediscount"></a>
# **DeleteCommerceDiscount**
> DeleteCommerceDiscount200Response DeleteCommerceDiscount (string discountId, string accountId)

Delete a discount

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
    public class DeleteCommerceDiscountExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var discountId = "discountId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Delete a discount
                DeleteCommerceDiscount200Response result = apiInstance.DeleteCommerceDiscount(discountId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceDiscount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceDiscountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a discount
    ApiResponse<DeleteCommerceDiscount200Response> response = apiInstance.DeleteCommerceDiscountWithHttpInfo(discountId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceDiscountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **discountId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**DeleteCommerceDiscount200Response**](DeleteCommerceDiscount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercemarketingactivity"></a>
# **DeleteCommerceMarketingActivity**
> DeleteCommerceMarketingActivity200Response DeleteCommerceMarketingActivity (string remoteId, string accountId)

Delete a marketing activity

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
    public class DeleteCommerceMarketingActivityExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var remoteId = "remoteId_example";  // string | The remoteId given when recording it.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Delete a marketing activity
                DeleteCommerceMarketingActivity200Response result = apiInstance.DeleteCommerceMarketingActivity(remoteId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceMarketingActivity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceMarketingActivityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a marketing activity
    ApiResponse<DeleteCommerceMarketingActivity200Response> response = apiInstance.DeleteCommerceMarketingActivityWithHttpInfo(remoteId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceMarketingActivityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **remoteId** | **string** | The remoteId given when recording it. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**DeleteCommerceMarketingActivity200Response**](DeleteCommerceMarketingActivity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Activity deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercemenu"></a>
# **DeleteCommerceMenu**
> DeleteCommerceMenu200Response DeleteCommerceMenu (string menuId, string accountId)

Delete a navigation menu

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
    public class DeleteCommerceMenuExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var menuId = "menuId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Delete a navigation menu
                DeleteCommerceMenu200Response result = apiInstance.DeleteCommerceMenu(menuId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceMenu: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceMenuWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a navigation menu
    ApiResponse<DeleteCommerceMenu200Response> response = apiInstance.DeleteCommerceMenuWithHttpInfo(menuId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceMenuWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **menuId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**DeleteCommerceMenu200Response**](DeleteCommerceMenu200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Menu deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercemetaobject"></a>
# **DeleteCommerceMetaobject**
> DeleteCommerceMetaobject200Response DeleteCommerceMetaobject (string metaobjectId, string accountId)

Delete a metaobject

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
    public class DeleteCommerceMetaobjectExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var metaobjectId = "metaobjectId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Delete a metaobject
                DeleteCommerceMetaobject200Response result = apiInstance.DeleteCommerceMetaobject(metaobjectId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceMetaobject: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceMetaobjectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a metaobject
    ApiResponse<DeleteCommerceMetaobject200Response> response = apiInstance.DeleteCommerceMetaobjectWithHttpInfo(metaobjectId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceMetaobjectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **metaobjectId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**DeleteCommerceMetaobject200Response**](DeleteCommerceMetaobject200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metaobject deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercepage"></a>
# **DeleteCommercePage**
> DeleteCommercePage200Response DeleteCommercePage (string pageId, string accountId)

Delete a page

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
    public class DeleteCommercePageExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var pageId = "pageId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Delete a page
                DeleteCommercePage200Response result = apiInstance.DeleteCommercePage(pageId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommercePage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommercePageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a page
    ApiResponse<DeleteCommercePage200Response> response = apiInstance.DeleteCommercePageWithHttpInfo(pageId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommercePageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**DeleteCommercePage200Response**](DeleteCommercePage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Page deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommercepricelistprices"></a>
# **DeleteCommercePriceListPrices**
> DeleteCommercePriceListPrices200Response DeleteCommercePriceListPrices (string priceListId, string accountId, string variantIds)

Remove fixed prices

The variants go back to the market's converted price. 

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
    public class DeleteCommercePriceListPricesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var priceListId = "priceListId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var variantIds = "variantIds_example";  // string | Comma-separated ids.

            try
            {
                // Remove fixed prices
                DeleteCommercePriceListPrices200Response result = apiInstance.DeleteCommercePriceListPrices(priceListId, accountId, variantIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommercePriceListPrices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommercePriceListPricesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove fixed prices
    ApiResponse<DeleteCommercePriceListPrices200Response> response = apiInstance.DeleteCommercePriceListPricesWithHttpInfo(priceListId, accountId, variantIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommercePriceListPricesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **priceListId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **variantIds** | **string** | Comma-separated ids. |  |

### Return type

[**DeleteCommercePriceListPrices200Response**](DeleteCommercePriceListPrices200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Prices removed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommerceproductoptions"></a>
# **DeleteCommerceProductOptions**
> CreateCommerceProduct201Response DeleteCommerceProductOptions (string productId, string accountId, string names)

Delete options

Deletes options by name, with the variants that depended on them. 

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
    public class DeleteCommerceProductOptionsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var names = "names_example";  // string | Comma-separated option names.

            try
            {
                // Delete options
                CreateCommerceProduct201Response result = apiInstance.DeleteCommerceProductOptions(productId, accountId, names);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceProductOptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceProductOptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete options
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.DeleteCommerceProductOptionsWithHttpInfo(productId, accountId, names);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceProductOptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **names** | **string** | Comma-separated option names. |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommerceproductvariants"></a>
# **DeleteCommerceProductVariants**
> CreateCommerceProduct201Response DeleteCommerceProductVariants (string productId, string accountId, string variantIds)

Delete variants

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
    public class DeleteCommerceProductVariantsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var variantIds = "variantIds_example";  // string | Comma-separated ids.

            try
            {
                // Delete variants
                CreateCommerceProduct201Response result = apiInstance.DeleteCommerceProductVariants(productId, accountId, variantIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceProductVariants: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceProductVariantsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete variants
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.DeleteCommerceProductVariantsWithHttpInfo(productId, accountId, variantIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceProductVariantsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **variantIds** | **string** | Comma-separated ids. |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletecommerceredirect"></a>
# **DeleteCommerceRedirect**
> DeleteCommerceRedirect200Response DeleteCommerceRedirect (string redirectId, string accountId)

Delete a URL redirect

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
    public class DeleteCommerceRedirectExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var redirectId = "redirectId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Delete a URL redirect
                DeleteCommerceRedirect200Response result = apiInstance.DeleteCommerceRedirect(redirectId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteCommerceRedirect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCommerceRedirectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a URL redirect
    ApiResponse<DeleteCommerceRedirect200Response> response = apiInstance.DeleteCommerceRedirectWithHttpInfo(redirectId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteCommerceRedirectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **redirectId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**DeleteCommerceRedirect200Response**](DeleteCommerceRedirect200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Redirect deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteproductmetafields"></a>
# **DeleteProductMetafields**
> DeleteProductMetafields200Response DeleteProductMetafields (string productId, string accountId, string keys)

Delete product metafields

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
    public class DeleteProductMetafieldsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var keys = "keys_example";  // string | Comma-separated namespace.key pairs.

            try
            {
                // Delete product metafields
                DeleteProductMetafields200Response result = apiInstance.DeleteProductMetafields(productId, accountId, keys);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DeleteProductMetafields: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteProductMetafieldsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete product metafields
    ApiResponse<DeleteProductMetafields200Response> response = apiInstance.DeleteProductMetafieldsWithHttpInfo(productId, accountId, keys);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DeleteProductMetafieldsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **keys** | **string** | Comma-separated namespace.key pairs. |  |

### Return type

[**DeleteProductMetafields200Response**](DeleteProductMetafields200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metafields deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicatecommerceproduct"></a>
# **DuplicateCommerceProduct**
> CreateCommerceProduct201Response DuplicateCommerceProduct (string productId, DuplicateCommerceProductRequest duplicateCommerceProductRequest)

Duplicate a product

Copies a product with its options, variants and (by default) images. The copy starts as a draft. 

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
    public class DuplicateCommerceProductExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var duplicateCommerceProductRequest = new DuplicateCommerceProductRequest(); // DuplicateCommerceProductRequest | 

            try
            {
                // Duplicate a product
                CreateCommerceProduct201Response result = apiInstance.DuplicateCommerceProduct(productId, duplicateCommerceProductRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.DuplicateCommerceProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateCommerceProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate a product
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.DuplicateCommerceProductWithHttpInfo(productId, duplicateCommerceProductRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.DuplicateCommerceProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **duplicateCommerceProductRequest** | [**DuplicateCommerceProductRequest**](DuplicateCommerceProductRequest.md) |  |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product duplicated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommercecatalogsync"></a>
# **GetCommerceCatalogSync**
> CreateCommerceCatalogSync202Response GetCommerceCatalogSync (string syncId)

Get a catalog sync

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
    public class GetCommerceCatalogSyncExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var syncId = "syncId_example";  // string | 

            try
            {
                // Get a catalog sync
                CreateCommerceCatalogSync202Response result = apiInstance.GetCommerceCatalogSync(syncId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommerceCatalogSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommerceCatalogSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a catalog sync
    ApiResponse<CreateCommerceCatalogSync202Response> response = apiInstance.GetCommerceCatalogSyncWithHttpInfo(syncId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommerceCatalogSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **syncId** | **string** |  |  |

### Return type

[**CreateCommerceCatalogSync202Response**](CreateCommerceCatalogSync202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog sync fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Catalog sync not found (code resource_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommercecollection"></a>
# **GetCommerceCollection**
> CreateCommerceCollection201Response GetCommerceCollection (string collectionId, string accountId)

Get a collection

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
    public class GetCommerceCollectionExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native collection id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Get a collection
                CreateCommerceCollection201Response result = apiInstance.GetCommerceCollection(collectionId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommerceCollection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommerceCollectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a collection
    ApiResponse<CreateCommerceCollection201Response> response = apiInstance.GetCommerceCollectionWithHttpInfo(collectionId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommerceCollectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native collection id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**CreateCommerceCollection201Response**](CreateCommerceCollection201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collection fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found (code account_not_found) or collection not found (code resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommercediscount"></a>
# **GetCommerceDiscount**
> CreateCommerceDiscount201Response GetCommerceDiscount (string discountId, string accountId)

Get a discount

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
    public class GetCommerceDiscountExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var discountId = "discountId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Get a discount
                CreateCommerceDiscount201Response result = apiInstance.GetCommerceDiscount(discountId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommerceDiscount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommerceDiscountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a discount
    ApiResponse<CreateCommerceDiscount201Response> response = apiInstance.GetCommerceDiscountWithHttpInfo(discountId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommerceDiscountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **discountId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**CreateCommerceDiscount201Response**](CreateCommerceDiscount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommercemenu"></a>
# **GetCommerceMenu**
> CreateCommerceMenu201Response GetCommerceMenu (string menuId, string accountId)

Get a navigation menu

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
    public class GetCommerceMenuExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var menuId = "menuId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Get a navigation menu
                CreateCommerceMenu201Response result = apiInstance.GetCommerceMenu(menuId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommerceMenu: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommerceMenuWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a navigation menu
    ApiResponse<CreateCommerceMenu201Response> response = apiInstance.GetCommerceMenuWithHttpInfo(menuId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommerceMenuWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **menuId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**CreateCommerceMenu201Response**](CreateCommerceMenu201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Menu fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommercemetaobject"></a>
# **GetCommerceMetaobject**
> CreateCommerceMetaobject201Response GetCommerceMetaobject (string metaobjectId, string accountId)

Get a metaobject

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
    public class GetCommerceMetaobjectExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var metaobjectId = "metaobjectId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Get a metaobject
                CreateCommerceMetaobject201Response result = apiInstance.GetCommerceMetaobject(metaobjectId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommerceMetaobject: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommerceMetaobjectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a metaobject
    ApiResponse<CreateCommerceMetaobject201Response> response = apiInstance.GetCommerceMetaobjectWithHttpInfo(metaobjectId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommerceMetaobjectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **metaobjectId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**CreateCommerceMetaobject201Response**](CreateCommerceMetaobject201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metaobject fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommercepage"></a>
# **GetCommercePage**
> CreateCommercePage201Response GetCommercePage (string pageId, string accountId)

Get a page

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
    public class GetCommercePageExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var pageId = "pageId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Get a page
                CreateCommercePage201Response result = apiInstance.GetCommercePage(pageId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommercePage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommercePageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a page
    ApiResponse<CreateCommercePage201Response> response = apiInstance.GetCommercePageWithHttpInfo(pageId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommercePageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**CreateCommercePage201Response**](CreateCommercePage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Page fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommerceproduct"></a>
# **GetCommerceProduct**
> CreateCommerceProduct201Response GetCommerceProduct (string productId, string accountId)

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
    public class GetCommerceProductExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native product id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Get a product
                CreateCommerceProduct201Response result = apiInstance.GetCommerceProduct(productId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommerceProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommerceProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a product
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.GetCommerceProductWithHttpInfo(productId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommerceProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native product id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

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
| **404** | Account not found (code account_not_found) or product not found (code product_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcommercestore"></a>
# **GetCommerceStore**
> GetCommerceStore200Response GetCommerceStore (string accountId)

Get a store

Returns the connected store with its currency, country and the `capabilities` it supports, so an integration can tell up front which Commerce operations the store serves. On Shopify, stock, sales channels, discounts, navigation, metaobjects, markets, marketing and image removal need permissions the store owner approves separately: `missingCapabilities` lists what is not granted yet and `grantPermissionsUrl` is the page where the owner approves it. 

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
    public class GetCommerceStoreExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // Get a store
                GetCommerceStore200Response result = apiInstance.GetCommerceStore(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.GetCommerceStore: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCommerceStoreWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a store
    ApiResponse<GetCommerceStore200Response> response = apiInstance.GetCommerceStoreWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.GetCommerceStoreWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**GetCommerceStore200Response**](GetCommerceStore200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Store fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcollectionmetafields"></a>
# **ListCollectionMetafields**
> ListProductMetafields200Response ListCollectionMetafields (string collectionId, string accountId)

List collection metafields

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
    public class ListCollectionMetafieldsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List collection metafields
                ListProductMetafields200Response result = apiInstance.ListCollectionMetafields(collectionId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCollectionMetafields: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCollectionMetafieldsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List collection metafields
    ApiResponse<ListProductMetafields200Response> response = apiInstance.ListCollectionMetafieldsWithHttpInfo(collectionId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCollectionMetafieldsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListProductMetafields200Response**](ListProductMetafields200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metafields listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercecatalogsyncs"></a>
# **ListCommerceCatalogSyncs**
> ListCommerceCatalogSyncs200Response ListCommerceCatalogSyncs (string accountId)

List catalog syncs

The ad-platform catalogs this store is kept in sync with.

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
    public class ListCommerceCatalogSyncsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List catalog syncs
                ListCommerceCatalogSyncs200Response result = apiInstance.ListCommerceCatalogSyncs(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceCatalogSyncs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceCatalogSyncsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List catalog syncs
    ApiResponse<ListCommerceCatalogSyncs200Response> response = apiInstance.ListCommerceCatalogSyncsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceCatalogSyncsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListCommerceCatalogSyncs200Response**](ListCommerceCatalogSyncs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog syncs listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercechannels"></a>
# **ListCommerceChannels**
> ListCommerceChannels200Response ListCommerceChannels (string accountId)

List sales channels

Where products and collections can be published: the online store, Shop, POS and installed channel apps. 

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
    public class ListCommerceChannelsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List sales channels
                ListCommerceChannels200Response result = apiInstance.ListCommerceChannels(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceChannels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceChannelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List sales channels
    ApiResponse<ListCommerceChannels200Response> response = apiInstance.ListCommerceChannelsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceChannelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListCommerceChannels200Response**](ListCommerceChannels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Channels listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercecollections"></a>
# **ListCommerceCollections**
> ListCommerceCollections200Response ListCommerceCollections (string accountId, int? limit = null, string? cursor = null, string? query = null)

List collections

Lists the store's product collections. Cursor-paginated like products. List a collection's products with `GET /v1/commerce/products?collectionId=...`. 

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
    public class ListCommerceCollectionsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? |  (optional) 
            var query = "query_example";  // string? | Platform collection search syntax (Shopify: title, handle, collection_type, ...). (optional) 

            try
            {
                // List collections
                ListCommerceCollections200Response result = apiInstance.ListCommerceCollections(accountId, limit, cursor, query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceCollections: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceCollectionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List collections
    ApiResponse<ListCommerceCollections200Response> response = apiInstance.ListCommerceCollectionsWithHttpInfo(accountId, limit, cursor, query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceCollectionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** |  | [optional]  |
| **query** | **string?** | Platform collection search syntax (Shopify: title, handle, collection_type, ...). | [optional]  |

### Return type

[**ListCommerceCollections200Response**](ListCommerceCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collections listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found (code account_not_found) or collection not found (code resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercediscounts"></a>
# **ListCommerceDiscounts**
> ListCommerceDiscounts200Response ListCommerceDiscounts (string accountId, int? limit = null, string? cursor = null, string? query = null)

List discounts

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
    public class ListCommerceDiscountsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? |  (optional) 
            var query = "query_example";  // string? | Platform search syntax, passed through. (optional) 

            try
            {
                // List discounts
                ListCommerceDiscounts200Response result = apiInstance.ListCommerceDiscounts(accountId, limit, cursor, query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceDiscounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceDiscountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List discounts
    ApiResponse<ListCommerceDiscounts200Response> response = apiInstance.ListCommerceDiscountsWithHttpInfo(accountId, limit, cursor, query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceDiscountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** |  | [optional]  |
| **query** | **string?** | Platform search syntax, passed through. | [optional]  |

### Return type

[**ListCommerceDiscounts200Response**](ListCommerceDiscounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discounts listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommerceinventory"></a>
# **ListCommerceInventory**
> ListCommerceInventory200Response ListCommerceInventory (string accountId, string productId)

Get a product's stock

Stock per variant and location: available, on hand, committed to orders and incoming. 

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
    public class ListCommerceInventoryExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var productId = "productId_example";  // string | 

            try
            {
                // Get a product's stock
                ListCommerceInventory200Response result = apiInstance.ListCommerceInventory(accountId, productId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceInventory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceInventoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a product's stock
    ApiResponse<ListCommerceInventory200Response> response = apiInstance.ListCommerceInventoryWithHttpInfo(accountId, productId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceInventoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **productId** | **string** |  |  |

### Return type

[**ListCommerceInventory200Response**](ListCommerceInventory200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stock fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercelocations"></a>
# **ListCommerceLocations**
> ListCommerceLocations200Response ListCommerceLocations (string accountId)

List locations

The store's stock locations (warehouses, shops). 

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
    public class ListCommerceLocationsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List locations
                ListCommerceLocations200Response result = apiInstance.ListCommerceLocations(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List locations
    ApiResponse<ListCommerceLocations200Response> response = apiInstance.ListCommerceLocationsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListCommerceLocations200Response**](ListCommerceLocations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Locations listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercemarkets"></a>
# **ListCommerceMarkets**
> ListCommerceMarkets200Response ListCommerceMarkets (string accountId)

List markets

The regions the store sells to, each with its own currency and pricing. 

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
    public class ListCommerceMarketsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List markets
                ListCommerceMarkets200Response result = apiInstance.ListCommerceMarkets(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<ListCommerceMarkets200Response> response = apiInstance.ListCommerceMarketsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceMarketsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListCommerceMarkets200Response**](ListCommerceMarkets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Markets listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercemenus"></a>
# **ListCommerceMenus**
> ListCommerceMenus200Response ListCommerceMenus (string accountId)

List navigation menus

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
    public class ListCommerceMenusExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List navigation menus
                ListCommerceMenus200Response result = apiInstance.ListCommerceMenus(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceMenus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceMenusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List navigation menus
    ApiResponse<ListCommerceMenus200Response> response = apiInstance.ListCommerceMenusWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceMenusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListCommerceMenus200Response**](ListCommerceMenus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Menus listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercemetaobjectdefinitions"></a>
# **ListCommerceMetaobjectDefinitions**
> ListCommerceMetaobjectDefinitions200Response ListCommerceMetaobjectDefinitions (string accountId)

List metaobject definitions

The custom content types defined on the store and their fields. 

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
    public class ListCommerceMetaobjectDefinitionsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List metaobject definitions
                ListCommerceMetaobjectDefinitions200Response result = apiInstance.ListCommerceMetaobjectDefinitions(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceMetaobjectDefinitions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceMetaobjectDefinitionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List metaobject definitions
    ApiResponse<ListCommerceMetaobjectDefinitions200Response> response = apiInstance.ListCommerceMetaobjectDefinitionsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceMetaobjectDefinitionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListCommerceMetaobjectDefinitions200Response**](ListCommerceMetaobjectDefinitions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Definitions listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercemetaobjects"></a>
# **ListCommerceMetaobjects**
> ListCommerceMetaobjects200Response ListCommerceMetaobjects (string accountId, string type, int? limit = null, string? cursor = null)

List metaobjects of a type

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
    public class ListCommerceMetaobjectsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var type = "type_example";  // string | Definition type from GET /v1/commerce/metaobject-definitions.
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List metaobjects of a type
                ListCommerceMetaobjects200Response result = apiInstance.ListCommerceMetaobjects(accountId, type, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceMetaobjects: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceMetaobjectsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List metaobjects of a type
    ApiResponse<ListCommerceMetaobjects200Response> response = apiInstance.ListCommerceMetaobjectsWithHttpInfo(accountId, type, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceMetaobjectsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **type** | **string** | Definition type from GET /v1/commerce/metaobject-definitions. |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** |  | [optional]  |

### Return type

[**ListCommerceMetaobjects200Response**](ListCommerceMetaobjects200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metaobjects listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercepages"></a>
# **ListCommercePages**
> ListCommercePages200Response ListCommercePages (string accountId, int? limit = null, string? cursor = null, string? query = null)

List pages

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
    public class ListCommercePagesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? |  (optional) 
            var query = "query_example";  // string? | Platform search syntax, passed through. (optional) 

            try
            {
                // List pages
                ListCommercePages200Response result = apiInstance.ListCommercePages(accountId, limit, cursor, query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommercePages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommercePagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List pages
    ApiResponse<ListCommercePages200Response> response = apiInstance.ListCommercePagesWithHttpInfo(accountId, limit, cursor, query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommercePagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** |  | [optional]  |
| **query** | **string?** | Platform search syntax, passed through. | [optional]  |

### Return type

[**ListCommercePages200Response**](ListCommercePages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pages listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommercepricelists"></a>
# **ListCommercePriceLists**
> ListCommercePriceLists200Response ListCommercePriceLists (string accountId)

List price lists

Price lists hold fixed prices per variant for a market. 

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
    public class ListCommercePriceListsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List price lists
                ListCommercePriceLists200Response result = apiInstance.ListCommercePriceLists(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommercePriceLists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommercePriceListsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List price lists
    ApiResponse<ListCommercePriceLists200Response> response = apiInstance.ListCommercePriceListsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommercePriceListsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListCommercePriceLists200Response**](ListCommercePriceLists200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Price lists listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommerceproducts"></a>
# **ListCommerceProducts**
> ListCommerceProducts200Response ListCommerceProducts (string accountId, int? limit = null, string? cursor = null, CommerceProductStatus? status = null, string? query = null, string? collectionId = null)

List products

Lists the store's products with their variants, options and images. Cursor-paginated: pass `limit` (1-100, default 20) and the `cursor` from a previous response's `nextCursor`, which is null on the last page. Filter with `status` and/or `query` (the platform's product search syntax, passed through verbatim). A status the platform has no equivalent of returns an empty page. 

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
    public class ListCommerceProductsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? | Opaque cursor from a previous response. Omit for the first page. (optional) 
            var status = new CommerceProductStatus?(); // CommerceProductStatus? |  (optional) 
            var query = "query_example";  // string? | Platform product search syntax (Shopify: title, vendor, product_type, tag, sku, handle, ...). (optional) 
            var collectionId = "collectionId_example";  // string? | Only products in this collection. (optional) 

            try
            {
                // List products
                ListCommerceProducts200Response result = apiInstance.ListCommerceProducts(accountId, limit, cursor, status, query, collectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List products
    ApiResponse<ListCommerceProducts200Response> response = apiInstance.ListCommerceProductsWithHttpInfo(accountId, limit, cursor, status, query, collectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** | Opaque cursor from a previous response. Omit for the first page. | [optional]  |
| **status** | [**CommerceProductStatus?**](CommerceProductStatus?.md) |  | [optional]  |
| **query** | **string?** | Platform product search syntax (Shopify: title, vendor, product_type, tag, sku, handle, ...). | [optional]  |
| **collectionId** | **string?** | Only products in this collection. | [optional]  |

### Return type

[**ListCommerceProducts200Response**](ListCommerceProducts200Response.md)

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
| **403** | The platform rejected the request (code insufficient_permissions). A Shopify store connected before product access was added must be reconnected through GET /v1/connect/shopify. |  -  |
| **404** | Account not found or not accessible (code account_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcommerceredirects"></a>
# **ListCommerceRedirects**
> ListCommerceRedirects200Response ListCommerceRedirects (string accountId, int? limit = null, string? cursor = null, string? query = null)

List URL redirects

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
    public class ListCommerceRedirectsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var limit = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string? |  (optional) 
            var query = "query_example";  // string? | Platform search syntax, passed through. (optional) 

            try
            {
                // List URL redirects
                ListCommerceRedirects200Response result = apiInstance.ListCommerceRedirects(accountId, limit, cursor, query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListCommerceRedirects: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCommerceRedirectsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List URL redirects
    ApiResponse<ListCommerceRedirects200Response> response = apiInstance.ListCommerceRedirectsWithHttpInfo(accountId, limit, cursor, query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListCommerceRedirectsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **limit** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string?** |  | [optional]  |
| **query** | **string?** | Platform search syntax, passed through. | [optional]  |

### Return type

[**ListCommerceRedirects200Response**](ListCommerceRedirects200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Redirects listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listproductmetafields"></a>
# **ListProductMetafields**
> ListProductMetafields200Response ListProductMetafields (string productId, string accountId)

List product metafields

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
    public class ListProductMetafieldsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.

            try
            {
                // List product metafields
                ListProductMetafields200Response result = apiInstance.ListProductMetafields(productId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ListProductMetafields: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListProductMetafieldsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List product metafields
    ApiResponse<ListProductMetafields200Response> response = apiInstance.ListProductMetafieldsWithHttpInfo(productId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ListProductMetafieldsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |

### Return type

[**ListProductMetafields200Response**](ListProductMetafields200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metafields listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removecommerceproductimages"></a>
# **RemoveCommerceProductImages**
> CreateCommerceProduct201Response RemoveCommerceProductImages (string productId, string accountId, string imageIds)

Remove images

Removes images from the product by image id (the `id` on each image). The file stays in the store's media library. Needs the products.images_remove capability. 

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
    public class RemoveCommerceProductImagesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var accountId = "accountId_example";  // string | Connected store SocialAccount id.
            var imageIds = "imageIds_example";  // string | Comma-separated ids.

            try
            {
                // Remove images
                CreateCommerceProduct201Response result = apiInstance.RemoveCommerceProductImages(productId, accountId, imageIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.RemoveCommerceProductImages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveCommerceProductImagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove images
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.RemoveCommerceProductImagesWithHttpInfo(productId, accountId, imageIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.RemoveCommerceProductImagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **accountId** | **string** | Connected store SocialAccount id. |  |
| **imageIds** | **string** | Comma-separated ids. |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product after the change |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reordercommercecollectionproducts"></a>
# **ReorderCommerceCollectionProducts**
> ReorderCommerceProductImages200Response ReorderCommerceCollectionProducts (string collectionId, ReorderCommerceCollectionProductsRequest reorderCommerceCollectionProductsRequest)

Reorder products in a collection

Moves products to new 0-based positions. Only for collections sorted `manual`. 

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
    public class ReorderCommerceCollectionProductsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native id.
            var reorderCommerceCollectionProductsRequest = new ReorderCommerceCollectionProductsRequest(); // ReorderCommerceCollectionProductsRequest | 

            try
            {
                // Reorder products in a collection
                ReorderCommerceProductImages200Response result = apiInstance.ReorderCommerceCollectionProducts(collectionId, reorderCommerceCollectionProductsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ReorderCommerceCollectionProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReorderCommerceCollectionProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reorder products in a collection
    ApiResponse<ReorderCommerceProductImages200Response> response = apiInstance.ReorderCommerceCollectionProductsWithHttpInfo(collectionId, reorderCommerceCollectionProductsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ReorderCommerceCollectionProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native id. |  |
| **reorderCommerceCollectionProductsRequest** | [**ReorderCommerceCollectionProductsRequest**](ReorderCommerceCollectionProductsRequest.md) |  |  |

### Return type

[**ReorderCommerceProductImages200Response**](ReorderCommerceProductImages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reorder accepted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="reordercommerceproductimages"></a>
# **ReorderCommerceProductImages**
> ReorderCommerceProductImages200Response ReorderCommerceProductImages (string productId, ReorderCommerceProductImagesRequest reorderCommerceProductImagesRequest)

Reorder images

Puts the product's images in the given order; the first becomes the featured image. `pending` is true while the platform finishes in the background. 

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
    public class ReorderCommerceProductImagesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var reorderCommerceProductImagesRequest = new ReorderCommerceProductImagesRequest(); // ReorderCommerceProductImagesRequest | 

            try
            {
                // Reorder images
                ReorderCommerceProductImages200Response result = apiInstance.ReorderCommerceProductImages(productId, reorderCommerceProductImagesRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.ReorderCommerceProductImages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReorderCommerceProductImagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reorder images
    ApiResponse<ReorderCommerceProductImages200Response> response = apiInstance.ReorderCommerceProductImagesWithHttpInfo(productId, reorderCommerceProductImagesRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.ReorderCommerceProductImagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **reorderCommerceProductImagesRequest** | [**ReorderCommerceProductImagesRequest**](ReorderCommerceProductImagesRequest.md) |  |  |

### Return type

[**ReorderCommerceProductImages200Response**](ReorderCommerceProductImages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reorder accepted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="runcommercecatalogsync"></a>
# **RunCommerceCatalogSync**
> CreateCommerceCatalogSync202Response RunCommerceCatalogSync (string syncId)

Run a catalog sync now

Queues a full run. Poll GET /v1/commerce/catalog-syncs/{syncId} for the outcome.

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
    public class RunCommerceCatalogSyncExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var syncId = "syncId_example";  // string | 

            try
            {
                // Run a catalog sync now
                CreateCommerceCatalogSync202Response result = apiInstance.RunCommerceCatalogSync(syncId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.RunCommerceCatalogSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RunCommerceCatalogSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run a catalog sync now
    ApiResponse<CreateCommerceCatalogSync202Response> response = apiInstance.RunCommerceCatalogSyncWithHttpInfo(syncId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.RunCommerceCatalogSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **syncId** | **string** |  |  |

### Return type

[**CreateCommerceCatalogSync202Response**](CreateCommerceCatalogSync202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Run queued |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Catalog sync not found (code resource_not_found). |  -  |
| **409** | A run is already in progress (code catalog_sync_conflict). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setcollectionmetafields"></a>
# **SetCollectionMetafields**
> ListProductMetafields200Response SetCollectionMetafields (string collectionId, SetProductMetafieldsRequest setProductMetafieldsRequest)

Set collection metafields

Creates or updates custom fields by namespace and key. 

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
    public class SetCollectionMetafieldsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native id.
            var setProductMetafieldsRequest = new SetProductMetafieldsRequest(); // SetProductMetafieldsRequest | 

            try
            {
                // Set collection metafields
                ListProductMetafields200Response result = apiInstance.SetCollectionMetafields(collectionId, setProductMetafieldsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.SetCollectionMetafields: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetCollectionMetafieldsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set collection metafields
    ApiResponse<ListProductMetafields200Response> response = apiInstance.SetCollectionMetafieldsWithHttpInfo(collectionId, setProductMetafieldsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.SetCollectionMetafieldsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native id. |  |
| **setProductMetafieldsRequest** | [**SetProductMetafieldsRequest**](SetProductMetafieldsRequest.md) |  |  |

### Return type

[**ListProductMetafields200Response**](ListProductMetafields200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metafields set |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setcommercediscountactive"></a>
# **SetCommerceDiscountActive**
> CreateCommerceDiscount201Response SetCommerceDiscountActive (string discountId, SetCommerceDiscountActiveRequest setCommerceDiscountActiveRequest)

Activate or deactivate a discount

Deactivating ends the discount now; activating starts it now. 

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
    public class SetCommerceDiscountActiveExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var discountId = "discountId_example";  // string | Platform-native id.
            var setCommerceDiscountActiveRequest = new SetCommerceDiscountActiveRequest(); // SetCommerceDiscountActiveRequest | 

            try
            {
                // Activate or deactivate a discount
                CreateCommerceDiscount201Response result = apiInstance.SetCommerceDiscountActive(discountId, setCommerceDiscountActiveRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.SetCommerceDiscountActive: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetCommerceDiscountActiveWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Activate or deactivate a discount
    ApiResponse<CreateCommerceDiscount201Response> response = apiInstance.SetCommerceDiscountActiveWithHttpInfo(discountId, setCommerceDiscountActiveRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.SetCommerceDiscountActiveWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **discountId** | **string** | Platform-native id. |  |
| **setCommerceDiscountActiveRequest** | [**SetCommerceDiscountActiveRequest**](SetCommerceDiscountActiveRequest.md) |  |  |

### Return type

[**CreateCommerceDiscount201Response**](CreateCommerceDiscount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount state changed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setcommercepricelistprices"></a>
# **SetCommercePriceListPrices**
> SetCommercePriceListPrices200Response SetCommercePriceListPrices (string priceListId, SetCommercePriceListPricesRequest setCommercePriceListPricesRequest)

Set fixed prices

Sets fixed prices for variants in the price list's currency, overriding the converted price in that market. 

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
    public class SetCommercePriceListPricesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var priceListId = "priceListId_example";  // string | Platform-native id.
            var setCommercePriceListPricesRequest = new SetCommercePriceListPricesRequest(); // SetCommercePriceListPricesRequest | 

            try
            {
                // Set fixed prices
                SetCommercePriceListPrices200Response result = apiInstance.SetCommercePriceListPrices(priceListId, setCommercePriceListPricesRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.SetCommercePriceListPrices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetCommercePriceListPricesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set fixed prices
    ApiResponse<SetCommercePriceListPrices200Response> response = apiInstance.SetCommercePriceListPricesWithHttpInfo(priceListId, setCommercePriceListPricesRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.SetCommercePriceListPricesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **priceListId** | **string** | Platform-native id. |  |
| **setCommercePriceListPricesRequest** | [**SetCommercePriceListPricesRequest**](SetCommercePriceListPricesRequest.md) |  |  |

### Return type

[**SetCommercePriceListPrices200Response**](SetCommercePriceListPrices200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Prices set |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setproductmetafields"></a>
# **SetProductMetafields**
> ListProductMetafields200Response SetProductMetafields (string productId, SetProductMetafieldsRequest setProductMetafieldsRequest)

Set product metafields

Creates or updates custom fields by namespace and key. 

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
    public class SetProductMetafieldsExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native id.
            var setProductMetafieldsRequest = new SetProductMetafieldsRequest(); // SetProductMetafieldsRequest | 

            try
            {
                // Set product metafields
                ListProductMetafields200Response result = apiInstance.SetProductMetafields(productId, setProductMetafieldsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.SetProductMetafields: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetProductMetafieldsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set product metafields
    ApiResponse<ListProductMetafields200Response> response = apiInstance.SetProductMetafieldsWithHttpInfo(productId, setProductMetafieldsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.SetProductMetafieldsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native id. |  |
| **setProductMetafieldsRequest** | [**SetProductMetafieldsRequest**](SetProductMetafieldsRequest.md) |  |  |

### Return type

[**ListProductMetafields200Response**](ListProductMetafields200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metafields set |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommercecollection"></a>
# **UpdateCommerceCollection**
> CreateCommerceCollection201Response UpdateCommerceCollection (string collectionId, UpdateCommerceCollectionRequest updateCommerceCollectionRequest)

Update a collection

Partial update; at least one field besides accountId is required. Change membership with POST /v1/commerce/collections/{collectionId}/products.

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
    public class UpdateCommerceCollectionExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var collectionId = "collectionId_example";  // string | Platform-native collection id.
            var updateCommerceCollectionRequest = new UpdateCommerceCollectionRequest(); // UpdateCommerceCollectionRequest | 

            try
            {
                // Update a collection
                CreateCommerceCollection201Response result = apiInstance.UpdateCommerceCollection(collectionId, updateCommerceCollectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommerceCollection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommerceCollectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a collection
    ApiResponse<CreateCommerceCollection201Response> response = apiInstance.UpdateCommerceCollectionWithHttpInfo(collectionId, updateCommerceCollectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommerceCollectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collectionId** | **string** | Platform-native collection id. |  |
| **updateCommerceCollectionRequest** | [**UpdateCommerceCollectionRequest**](UpdateCommerceCollectionRequest.md) |  |  |

### Return type

[**CreateCommerceCollection201Response**](CreateCommerceCollection201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collection updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The platform rejected the request (code insufficient_permissions). Reconnect the store. |  -  |
| **404** | Account not found (code account_not_found) or collection not found (code resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommercediscount"></a>
# **UpdateCommerceDiscount**
> CreateCommerceDiscount201Response UpdateCommerceDiscount (string discountId, UpdateCommerceDiscountRequest updateCommerceDiscountRequest)

Update a discount

Changes a percentage, fixed-amount or free-shipping discount. Buy-X-get-Y and app discounts are read-only here. 

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
    public class UpdateCommerceDiscountExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var discountId = "discountId_example";  // string | Platform-native id.
            var updateCommerceDiscountRequest = new UpdateCommerceDiscountRequest(); // UpdateCommerceDiscountRequest | 

            try
            {
                // Update a discount
                CreateCommerceDiscount201Response result = apiInstance.UpdateCommerceDiscount(discountId, updateCommerceDiscountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommerceDiscount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommerceDiscountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a discount
    ApiResponse<CreateCommerceDiscount201Response> response = apiInstance.UpdateCommerceDiscountWithHttpInfo(discountId, updateCommerceDiscountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommerceDiscountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **discountId** | **string** | Platform-native id. |  |
| **updateCommerceDiscountRequest** | [**UpdateCommerceDiscountRequest**](UpdateCommerceDiscountRequest.md) |  |  |

### Return type

[**CreateCommerceDiscount201Response**](CreateCommerceDiscount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommercemenu"></a>
# **UpdateCommerceMenu**
> CreateCommerceMenu201Response UpdateCommerceMenu (string menuId, UpdateCommerceMenuRequest updateCommerceMenuRequest)

Replace a navigation menu

Replaces the title and the whole item tree. 

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
    public class UpdateCommerceMenuExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var menuId = "menuId_example";  // string | Platform-native id.
            var updateCommerceMenuRequest = new UpdateCommerceMenuRequest(); // UpdateCommerceMenuRequest | 

            try
            {
                // Replace a navigation menu
                CreateCommerceMenu201Response result = apiInstance.UpdateCommerceMenu(menuId, updateCommerceMenuRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommerceMenu: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommerceMenuWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace a navigation menu
    ApiResponse<CreateCommerceMenu201Response> response = apiInstance.UpdateCommerceMenuWithHttpInfo(menuId, updateCommerceMenuRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommerceMenuWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **menuId** | **string** | Platform-native id. |  |
| **updateCommerceMenuRequest** | [**UpdateCommerceMenuRequest**](UpdateCommerceMenuRequest.md) |  |  |

### Return type

[**CreateCommerceMenu201Response**](CreateCommerceMenu201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Menu updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommercemetaobject"></a>
# **UpdateCommerceMetaobject**
> CreateCommerceMetaobject201Response UpdateCommerceMetaobject (string metaobjectId, UpdateCommerceMetaobjectRequest updateCommerceMetaobjectRequest)

Update a metaobject

Sets the given field values; fields left out keep theirs. 

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
    public class UpdateCommerceMetaobjectExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var metaobjectId = "metaobjectId_example";  // string | Platform-native id.
            var updateCommerceMetaobjectRequest = new UpdateCommerceMetaobjectRequest(); // UpdateCommerceMetaobjectRequest | 

            try
            {
                // Update a metaobject
                CreateCommerceMetaobject201Response result = apiInstance.UpdateCommerceMetaobject(metaobjectId, updateCommerceMetaobjectRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommerceMetaobject: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommerceMetaobjectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a metaobject
    ApiResponse<CreateCommerceMetaobject201Response> response = apiInstance.UpdateCommerceMetaobjectWithHttpInfo(metaobjectId, updateCommerceMetaobjectRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommerceMetaobjectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **metaobjectId** | **string** | Platform-native id. |  |
| **updateCommerceMetaobjectRequest** | [**UpdateCommerceMetaobjectRequest**](UpdateCommerceMetaobjectRequest.md) |  |  |

### Return type

[**CreateCommerceMetaobject201Response**](CreateCommerceMetaobject201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metaobject updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommercepage"></a>
# **UpdateCommercePage**
> CreateCommercePage201Response UpdateCommercePage (string pageId, UpdateCommercePageRequest updateCommercePageRequest)

Update a page

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
    public class UpdateCommercePageExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var pageId = "pageId_example";  // string | Platform-native id.
            var updateCommercePageRequest = new UpdateCommercePageRequest(); // UpdateCommercePageRequest | 

            try
            {
                // Update a page
                CreateCommercePage201Response result = apiInstance.UpdateCommercePage(pageId, updateCommercePageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommercePage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommercePageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a page
    ApiResponse<CreateCommercePage201Response> response = apiInstance.UpdateCommercePageWithHttpInfo(pageId, updateCommercePageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommercePageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageId** | **string** | Platform-native id. |  |
| **updateCommercePageRequest** | [**UpdateCommercePageRequest**](UpdateCommercePageRequest.md) |  |  |

### Return type

[**CreateCommercePage201Response**](CreateCommercePage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Page updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommerceproduct"></a>
# **UpdateCommerceProduct**
> CreateCommerceProduct201Response UpdateCommerceProduct (string productId, UpdateCommerceProductRequest updateCommerceProductRequest)

Update a product

Partial-updates the product's own fields; at least one besides `accountId` is required. `tags` replaces the full list. Change prices with `POST /v1/commerce/products/{productId}/price` and status with `POST /v1/commerce/products/state`. 

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
    public class UpdateCommerceProductExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native product id.
            var updateCommerceProductRequest = new UpdateCommerceProductRequest(); // UpdateCommerceProductRequest | 

            try
            {
                // Update a product
                CreateCommerceProduct201Response result = apiInstance.UpdateCommerceProduct(productId, updateCommerceProductRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommerceProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommerceProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a product
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.UpdateCommerceProductWithHttpInfo(productId, updateCommerceProductRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommerceProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native product id. |  |
| **updateCommerceProductRequest** | [**UpdateCommerceProductRequest**](UpdateCommerceProductRequest.md) |  |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

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
| **404** | Account not found (code account_not_found) or product not found (code product_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommerceproductprices"></a>
# **UpdateCommerceProductPrices**
> CreateCommerceProduct201Response UpdateCommerceProductPrices (string productId, UpdateCommerceProductPricesRequest updateCommerceProductPricesRequest)

Update variant prices

Sets the price and/or compare-at price of the listed variants. Other variants are untouched. Amounts are in the store currency; send `compareAtPrice: null` to remove a strike-through price. 

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
    public class UpdateCommerceProductPricesExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Platform-native product id.
            var updateCommerceProductPricesRequest = new UpdateCommerceProductPricesRequest(); // UpdateCommerceProductPricesRequest | 

            try
            {
                // Update variant prices
                CreateCommerceProduct201Response result = apiInstance.UpdateCommerceProductPrices(productId, updateCommerceProductPricesRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommerceProductPrices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommerceProductPricesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update variant prices
    ApiResponse<CreateCommerceProduct201Response> response = apiInstance.UpdateCommerceProductPricesWithHttpInfo(productId, updateCommerceProductPricesRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommerceProductPricesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Platform-native product id. |  |
| **updateCommerceProductPricesRequest** | [**UpdateCommerceProductPricesRequest**](UpdateCommerceProductPricesRequest.md) |  |  |

### Return type

[**CreateCommerceProduct201Response**](CreateCommerceProduct201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Prices updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found (code account_not_found) or product not found (code product_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecommerceredirect"></a>
# **UpdateCommerceRedirect**
> CreateCommerceRedirect201Response UpdateCommerceRedirect (string redirectId, UpdateCommerceRedirectRequest updateCommerceRedirectRequest)

Update a URL redirect

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
    public class UpdateCommerceRedirectExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var redirectId = "redirectId_example";  // string | Platform-native id.
            var updateCommerceRedirectRequest = new UpdateCommerceRedirectRequest(); // UpdateCommerceRedirectRequest | 

            try
            {
                // Update a URL redirect
                CreateCommerceRedirect201Response result = apiInstance.UpdateCommerceRedirect(redirectId, updateCommerceRedirectRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpdateCommerceRedirect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCommerceRedirectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a URL redirect
    ApiResponse<CreateCommerceRedirect201Response> response = apiInstance.UpdateCommerceRedirectWithHttpInfo(redirectId, updateCommerceRedirectRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpdateCommerceRedirectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **redirectId** | **string** | Platform-native id. |  |
| **updateCommerceRedirectRequest** | [**UpdateCommerceRedirectRequest**](UpdateCommerceRedirectRequest.md) |  |  |

### Return type

[**CreateCommerceRedirect201Response**](CreateCommerceRedirect201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Redirect updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="upsertcommercemarketingactivity"></a>
# **UpsertCommerceMarketingActivity**
> UpsertCommerceMarketingActivity200Response UpsertCommerceMarketingActivity (UpsertCommerceMarketingActivityRequest upsertCommerceMarketingActivityRequest)

Record a marketing activity

Creates or updates (by `remoteId`) an activity in the store's Marketing section, so the merchant sees a post, ad or message you ran for them, with its link and UTM parameters for attribution. Use your own id (for example the Zernio post or ad id) as `remoteId`. 

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
    public class UpsertCommerceMarketingActivityExample
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
            var apiInstance = new CommerceApi(httpClient, config, httpClientHandler);
            var upsertCommerceMarketingActivityRequest = new UpsertCommerceMarketingActivityRequest(); // UpsertCommerceMarketingActivityRequest | 

            try
            {
                // Record a marketing activity
                UpsertCommerceMarketingActivity200Response result = apiInstance.UpsertCommerceMarketingActivity(upsertCommerceMarketingActivityRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CommerceApi.UpsertCommerceMarketingActivity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpsertCommerceMarketingActivityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Record a marketing activity
    ApiResponse<UpsertCommerceMarketingActivity200Response> response = apiInstance.UpsertCommerceMarketingActivityWithHttpInfo(upsertCommerceMarketingActivityRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CommerceApi.UpsertCommerceMarketingActivityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **upsertCommerceMarketingActivityRequest** | [**UpsertCommerceMarketingActivityRequest**](UpsertCommerceMarketingActivityRequest.md) |  |  |

### Return type

[**UpsertCommerceMarketingActivity200Response**](UpsertCommerceMarketingActivity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Activity recorded |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | The store has not granted this permission, or the token was revoked (code insufficient_permissions). Reconnect the store to grant the latest permissions; GET /v1/commerce/store lists what the current grant allows. |  -  |
| **404** | Account not found (code account_not_found) or the resource was not found (code product_not_found or resource_not_found). |  -  |
| **429** | Rate limited, either by Zernio or by the platform. Retry later. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

