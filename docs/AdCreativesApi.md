# Zernio.Api.AdCreativesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAdCreative**](AdCreativesApi.md#createadcreative) | **POST** /v1/ads/creatives | Create a standalone creative |
| [**DeleteAdCreative**](AdCreativesApi.md#deleteadcreative) | **DELETE** /v1/ads/creatives/{creativeId} | Delete a creative |
| [**DeleteAdVideo**](AdCreativesApi.md#deleteadvideo) | **DELETE** /v1/ads/videos/{videoId} | Delete an ad video |
| [**GenerateAdPreviews**](AdCreativesApi.md#generateadpreviews) | **POST** /v1/ads/preview | Render pre-create ad previews |
| [**GetAdCreative**](AdCreativesApi.md#getadcreative) | **GET** /v1/ads/creatives/{creativeId} | Creative details |
| [**GetAdMedia**](AdCreativesApi.md#getadmedia) | **GET** /v1/ads/{adId}/media | Direct video and image URLs for an ad |
| [**GetAdPreviews**](AdCreativesApi.md#getadpreviews) | **GET** /v1/ads/{adId}/preview | Render previews of an existing ad |
| [**ListAdCatalogProductSets**](AdCreativesApi.md#listadcatalogproductsets) | **GET** /v1/ads/catalogs/{catalogId}/product-sets | List a catalog&#39;s product sets |
| [**ListAdCatalogs**](AdCreativesApi.md#listadcatalogs) | **GET** /v1/ads/catalogs | List Meta product catalogs |
| [**ListAdCreatives**](AdCreativesApi.md#listadcreatives) | **GET** /v1/ads/creatives | Creative library |
| [**ListAdImages**](AdCreativesApi.md#listadimages) | **GET** /v1/ads/images | Ad image library |
| [**ListAdVideos**](AdCreativesApi.md#listadvideos) | **GET** /v1/ads/videos | Ad video library |
| [**UpdateAdCreative**](AdCreativesApi.md#updateadcreative) | **PUT** /v1/ads/creatives/{creativeId} | Rename a creative |
| [**UploadAdImage**](AdCreativesApi.md#uploadadimage) | **POST** /v1/ads/images | Upload an ad image from base64 |
| [**UploadAdVideo**](AdCreativesApi.md#uploadadvideo) | **POST** /v1/ads/videos | Upload an ad video |

<a id="createadcreative"></a>
# **CreateAdCreative**
> CreateAdCreative201Response CreateAdCreative (CreateAdCreativeRequest createAdCreativeRequest)

Create a standalone creative

Creates a creative in the library WITHOUT an ad, reusable on the create endpoints via `existingCreativeId`. Provide exactly one of `imageUrl` (uploaded server-side), `imageHash` (from POST /v1/ads/images or the library list), or `carouselCards` (2-10 hand-built cards). The Page (and linked Instagram account, when present) is resolved from `accountId` as the story actor.

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
    public class CreateAdCreativeExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var createAdCreativeRequest = new CreateAdCreativeRequest(); // CreateAdCreativeRequest | 

            try
            {
                // Create a standalone creative
                CreateAdCreative201Response result = apiInstance.CreateAdCreative(createAdCreativeRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.CreateAdCreative: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCreativeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a standalone creative
    ApiResponse<CreateAdCreative201Response> response = apiInstance.CreateAdCreativeWithHttpInfo(createAdCreativeRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.CreateAdCreativeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdCreativeRequest** | [**CreateAdCreativeRequest**](CreateAdCreativeRequest.md) |  |  |

### Return type

[**CreateAdCreative201Response**](CreateAdCreative201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Creative created |  -  |
| **400** | Invalid input, or Meta rejected the create |  -  |
| **401** | Unauthorized |  -  |
| **422** | No Facebook Page found to act as the story actor |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadcreative"></a>
# **DeleteAdCreative**
> DeleteAdCreative200Response DeleteAdCreative (string creativeId, string accountId)

Delete a creative

Deletes a creative from the library. Meta only allows deleting creatives not referenced by any ad — otherwise its 400 surfaces verbatim.

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
    public class DeleteAdCreativeExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var creativeId = "creativeId_example";  // string | Platform creative id
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.

            try
            {
                // Delete a creative
                DeleteAdCreative200Response result = apiInstance.DeleteAdCreative(creativeId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.DeleteAdCreative: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdCreativeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a creative
    ApiResponse<DeleteAdCreative200Response> response = apiInstance.DeleteAdCreativeWithHttpInfo(creativeId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.DeleteAdCreativeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creativeId** | **string** | Platform creative id |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |

### Return type

[**DeleteAdCreative200Response**](DeleteAdCreative200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Creative deleted |  -  |
| **400** | Invalid input, the creative is in use, or Meta rejected the delete |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadvideo"></a>
# **DeleteAdVideo**
> DeleteAdVideo200Response DeleteAdVideo (string videoId, string accountId, string adAccountId)

Delete an ad video

Removes a video from the ad account's video library. Meta's canonical `DELETE /{video_id}` fails with code 10 / subcode 1363055 for videos uploaded via `/act_X/advideos` even with `ads_management`; this endpoint uses the working account-scoped shape `DELETE /act_X/advideos?video_id=<id>` and returns Meta's `{success: true}` verbatim. Deleting a video that lives in a different ad account, or that Meta has already removed, returns Meta's error verbatim as a 4xx.

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
    public class DeleteAdVideoExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var videoId = "videoId_example";  // string | Meta ad video id (numeric).
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>) that owns the video.

            try
            {
                // Delete an ad video
                DeleteAdVideo200Response result = apiInstance.DeleteAdVideo(videoId, accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.DeleteAdVideo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdVideoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete an ad video
    ApiResponse<DeleteAdVideo200Response> response = apiInstance.DeleteAdVideoWithHttpInfo(videoId, accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.DeleteAdVideoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **videoId** | **string** | Meta ad video id (numeric). |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;) that owns the video. |  |

### Return type

[**DeleteAdVideo200Response**](DeleteAdVideo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Video deleted |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="generateadpreviews"></a>
# **GenerateAdPreviews**
> GenerateAdPreviews200Response GenerateAdPreviews (GenerateAdPreviewsRequest generateAdPreviewsRequest)

Render pre-create ad previews

Renders how a creative would look per placement BEFORE any ad exists, via Meta's `/generatepreviews`. Provide exactly one creative source: `existingCreativeId` or `creativeSpec`. Each preview is an HTML `<iframe>` snippet embeddable directly. Unknown `formats` values return Meta's 400 verbatim. 

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
    public class GenerateAdPreviewsExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var generateAdPreviewsRequest = new GenerateAdPreviewsRequest(); // GenerateAdPreviewsRequest | 

            try
            {
                // Render pre-create ad previews
                GenerateAdPreviews200Response result = apiInstance.GenerateAdPreviews(generateAdPreviewsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.GenerateAdPreviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GenerateAdPreviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Render pre-create ad previews
    ApiResponse<GenerateAdPreviews200Response> response = apiInstance.GenerateAdPreviewsWithHttpInfo(generateAdPreviewsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.GenerateAdPreviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **generateAdPreviewsRequest** | [**GenerateAdPreviewsRequest**](GenerateAdPreviewsRequest.md) |  |  |

### Return type

[**GenerateAdPreviews200Response**](GenerateAdPreviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rendered previews |  -  |
| **400** | Invalid input, or Meta rejected the creative spec / ad_format — message carries Meta&#39;s error |  -  |
| **401** | Unauthorized |  -  |
| **429** | Meta rate limit reached |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcreative"></a>
# **GetAdCreative**
> GetAdCreative200Response GetAdCreative (string creativeId, string accountId, string? fields = null)

Creative details

One creative's details, verbatim from Meta. `fields` is a raw-passthrough override of the default projection.

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
    public class GetAdCreativeExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var creativeId = "creativeId_example";  // string | Platform creative id
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var fields = "fields_example";  // string? | Comma-separated Graph field override (supports nested {} projections). (optional) 

            try
            {
                // Creative details
                GetAdCreative200Response result = apiInstance.GetAdCreative(creativeId, accountId, fields);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.GetAdCreative: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCreativeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creative details
    ApiResponse<GetAdCreative200Response> response = apiInstance.GetAdCreativeWithHttpInfo(creativeId, accountId, fields);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.GetAdCreativeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creativeId** | **string** | Platform creative id |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **fields** | **string?** | Comma-separated Graph field override (supports nested {} projections). | [optional]  |

### Return type

[**GetAdCreative200Response**](GetAdCreative200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Creative details |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadmedia"></a>
# **GetAdMedia**
> GetAdMedia200Response GetAdMedia (string adId)

Direct video and image URLs for an ad

Returns the direct signed URLs for every video and image asset used by an ad's live creative, normalised across shapes: single image/video, carousel, Reels/Story (`object_story_spec.video_data`) and dynamic creative (`asset_feed_spec`). Video items include Meta's poster thumbnail and the video's Meta id when available.  Reads Meta live rather than the stored creative blob because Meta's signed fbcdn URLs carry an `oe=<hex>` expiration (image_url ~24 h, video source ~12 d). Treat URLs as short-lived — re-fetch this endpoint before serving or downloading assets instead of caching URLs beyond that window.

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
    public class GetAdMediaExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Zernio ad id (24-char hex) or platform ad id.

            try
            {
                // Direct video and image URLs for an ad
                GetAdMedia200Response result = apiInstance.GetAdMedia(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.GetAdMedia: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdMediaWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Direct video and image URLs for an ad
    ApiResponse<GetAdMedia200Response> response = apiInstance.GetAdMediaWithHttpInfo(adId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.GetAdMediaWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Zernio ad id (24-char hex) or platform ad id. |  |

### Return type

[**GetAdMedia200Response**](GetAdMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Media assets |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad not found |  -  |
| **422** | No active Meta connection for this ad. Reconnect the account. |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadpreviews"></a>
# **GetAdPreviews**
> GetAdPreviews200Response GetAdPreviews (string adId, string? formats = null)

Render previews of an existing ad

Renders an EXISTING ad per placement via Meta's `/{ad_id}/previews`. Each preview is an HTML `<iframe>` snippet embeddable directly. Unknown `formats` values return Meta's 400 verbatim. 

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
    public class GetAdPreviewsExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Zernio ad id (24-char hex).
            var formats = "formats_example";  // string? | Comma-separated Meta ad_format values (max 10), one preview per format. Defaults to DESKTOP_FEED_STANDARD. (optional) 

            try
            {
                // Render previews of an existing ad
                GetAdPreviews200Response result = apiInstance.GetAdPreviews(adId, formats);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.GetAdPreviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdPreviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Render previews of an existing ad
    ApiResponse<GetAdPreviews200Response> response = apiInstance.GetAdPreviewsWithHttpInfo(adId, formats);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.GetAdPreviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Zernio ad id (24-char hex). |  |
| **formats** | **string?** | Comma-separated Meta ad_format values (max 10), one preview per format. Defaults to DESKTOP_FEED_STANDARD. | [optional]  |

### Return type

[**GetAdPreviews200Response**](GetAdPreviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rendered previews |  -  |
| **400** | Invalid input, or Meta rejected the ad_format — message carries Meta&#39;s error |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad not found |  -  |
| **429** | Meta rate limit reached |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcatalogproductsets"></a>
# **ListAdCatalogProductSets**
> ListAdCatalogProductSets200Response ListAdCatalogProductSets (string catalogId, string accountId)

List a catalog's product sets

Lists a Meta product catalog's product sets — the unit a catalog ad promotes. Pass the chosen set as `promotedObject.productSetId` on POST /v1/ads/create with `goal: catalog_sales`.

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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var catalogId = "catalogId_example";  // string | Meta product catalog ID (from GET /v1/ads/catalogs)
            var accountId = "accountId_example";  // string | A facebook, instagram, or metaads social account ID

            try
            {
                // List a catalog's product sets
                ListAdCatalogProductSets200Response result = apiInstance.ListAdCatalogProductSets(catalogId, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.ListAdCatalogProductSets: " + e.Message);
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
    ApiResponse<ListAdCatalogProductSets200Response> response = apiInstance.ListAdCatalogProductSetsWithHttpInfo(catalogId, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.ListAdCatalogProductSetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **catalogId** | **string** | Meta product catalog ID (from GET /v1/ads/catalogs) |  |
| **accountId** | **string** | A facebook, instagram, or metaads social account ID |  |

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
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcatalogs"></a>
# **ListAdCatalogs**
> ListAdCatalogs200Response ListAdCatalogs (string accountId, string adAccountId)

List Meta product catalogs

Lists the Meta product catalogs reachable from an ad account (owned + agency-shared catalogs of the ad account's business), for Advantage+ catalog ads (`goal: catalog_sales` on POST /v1/ads/create — e.g. vehicle inventory catalogs). Read-only; uses scopes customers already granted (no reconnect needed). Catalog contents (items, feeds) are managed in Meta Commerce Manager, not through this API.

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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | A facebook, instagram, or metaads social account ID
            var adAccountId = "adAccountId_example";  // string | Meta ad account ID (act_...)

            try
            {
                // List Meta product catalogs
                ListAdCatalogs200Response result = apiInstance.ListAdCatalogs(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.ListAdCatalogs: " + e.Message);
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
    ApiResponse<ListAdCatalogs200Response> response = apiInstance.ListAdCatalogsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.ListAdCatalogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | A facebook, instagram, or metaads social account ID |  |
| **adAccountId** | **string** | Meta ad account ID (act_...) |  |

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
| **200** | Catalogs |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcreatives"></a>
# **ListAdCreatives**
> ListAdCreatives200Response ListAdCreatives (string accountId, string adAccountId, string? fields = null, int? limit = null, string? after = null)

Creative library

Lists the ad account's creative library (Meta's `/act_X/adcreatives`), rows returned verbatim. The default projection covers id, name, status, object type, thumbnail, object_story_spec / asset_feed_spec and url_tags; `fields` is a raw-passthrough override. Any creative id here is reusable on the create endpoints via `existingCreativeId`.

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
    public class ListAdCreativesExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var fields = "fields_example";  // string? | Comma-separated Graph field override (supports nested {} projections). (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Creative library
                ListAdCreatives200Response result = apiInstance.ListAdCreatives(accountId, adAccountId, fields, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.ListAdCreatives: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCreativesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creative library
    ApiResponse<ListAdCreatives200Response> response = apiInstance.ListAdCreativesWithHttpInfo(accountId, adAccountId, fields, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.ListAdCreativesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **fields** | **string?** | Comma-separated Graph field override (supports nested {} projections). | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListAdCreatives200Response**](ListAdCreatives200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Creatives (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadimages"></a>
# **ListAdImages**
> ListAdImages200Response ListAdImages (string accountId, string adAccountId, string? fields = null, int? limit = null, string? after = null)

Ad image library

Lists the ad account's image library (Meta's `/act_X/adimages`), rows returned verbatim. The default projection covers hash, url, name, dimensions and status; `fields` is a raw-passthrough override. Any `hash` here is reusable wherever Meta accepts `image_hash` (e.g. `imageHash` on POST /v1/ads/creatives).

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
    public class ListAdImagesExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var fields = "fields_example";  // string? | Comma-separated Graph field override (supports nested {} projections). (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Ad image library
                ListAdImages200Response result = apiInstance.ListAdImages(accountId, adAccountId, fields, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.ListAdImages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdImagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad image library
    ApiResponse<ListAdImages200Response> response = apiInstance.ListAdImagesWithHttpInfo(accountId, adAccountId, fields, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.ListAdImagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **fields** | **string?** | Comma-separated Graph field override (supports nested {} projections). | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListAdImages200Response**](ListAdImages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad images (raw Meta shape) |  -  |
| **400** | Invalid input, or Meta rejected the query |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadvideos"></a>
# **ListAdVideos**
> ListAdVideos200Response ListAdVideos (string accountId, string adAccountId, string? fields = null, int? limit = null, string? after = null)

Ad video library

Lists the ad account's video library (Meta's `/act_X/advideos`), rows returned verbatim. The default projection covers id, title, status, poster frames and length; `fields` is a raw-passthrough override. Any `id` here is reusable as `video.id` on the create endpoints, so N ads that differ only in copy share one upload.  This is the only way to reach a video uploaded OUTSIDE Zernio (Ads Manager, another tool); videos we uploaded also come back as `creative.videoId` on GET /v1/ads.  Meta transcodes asynchronously, so a row is only usable once `status.video_status` reads `ready`. Upload a new video via POST /v1/ads/videos, or inline via `video.url` on POST /v1/ads/create.

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
    public class ListAdVideosExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var adAccountId = "adAccountId_example";  // string | Meta ad account id (act_<n>).
            var fields = "fields_example";  // string? | Comma-separated Graph field override (supports nested {} projections). (optional) 
            var limit = 25;  // int? | Rows per page (optional)  (default to 25)
            var after = "after_example";  // string? | Cursor from paging.after of the previous page. (optional) 

            try
            {
                // Ad video library
                ListAdVideos200Response result = apiInstance.ListAdVideos(accountId, adAccountId, fields, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.ListAdVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ad video library
    ApiResponse<ListAdVideos200Response> response = apiInstance.ListAdVideosWithHttpInfo(accountId, adAccountId, fields, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.ListAdVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **adAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). |  |
| **fields** | **string?** | Comma-separated Graph field override (supports nested {} projections). | [optional]  |
| **limit** | **int?** | Rows per page | [optional] [default to 25] |
| **after** | **string?** | Cursor from paging.after of the previous page. | [optional]  |

### Return type

[**ListAdVideos200Response**](ListAdVideos200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad videos (raw Meta shape) |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadcreative"></a>
# **UpdateAdCreative**
> UpdateAdCreative200Response UpdateAdCreative (string creativeId, UpdateAdCreativeRequest updateAdCreativeRequest)

Rename a creative

Renames a creative. Creatives are immutable on Meta beyond `name` — for content changes create a new creative (POST /v1/ads/creatives) and swap it onto the ad (PUT /v1/ads/{adId} with `creative`).

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
    public class UpdateAdCreativeExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var creativeId = "creativeId_example";  // string | Platform creative id
            var updateAdCreativeRequest = new UpdateAdCreativeRequest(); // UpdateAdCreativeRequest | 

            try
            {
                // Rename a creative
                UpdateAdCreative200Response result = apiInstance.UpdateAdCreative(creativeId, updateAdCreativeRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.UpdateAdCreative: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdCreativeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rename a creative
    ApiResponse<UpdateAdCreative200Response> response = apiInstance.UpdateAdCreativeWithHttpInfo(creativeId, updateAdCreativeRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.UpdateAdCreativeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creativeId** | **string** | Platform creative id |  |
| **updateAdCreativeRequest** | [**UpdateAdCreativeRequest**](UpdateAdCreativeRequest.md) |  |  |

### Return type

[**UpdateAdCreative200Response**](UpdateAdCreative200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Creative renamed |  -  |
| **400** | Invalid input, or Meta rejected the update |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadadimage"></a>
# **UploadAdImage**
> UploadAdImage201Response UploadAdImage (UploadAdImageRequest uploadAdImageRequest)

Upload an ad image from base64

Uploads raw image bytes to the Meta ad account's image library — for callers whose creatives aren't hosted at a public URL. Returns the image `hash` (Meta's identifier for the asset) and the Meta-hosted `url`, which can be used directly as `imageUrl` on the create endpoints. Max 30 MB decoded.

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
    public class UploadAdImageExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var uploadAdImageRequest = new UploadAdImageRequest(); // UploadAdImageRequest | 

            try
            {
                // Upload an ad image from base64
                UploadAdImage201Response result = apiInstance.UploadAdImage(uploadAdImageRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.UploadAdImage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadAdImageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload an ad image from base64
    ApiResponse<UploadAdImage201Response> response = apiInstance.UploadAdImageWithHttpInfo(uploadAdImageRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.UploadAdImageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **uploadAdImageRequest** | [**UploadAdImageRequest**](UploadAdImageRequest.md) |  |  |

### Return type

[**UploadAdImage201Response**](UploadAdImage201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Image uploaded |  -  |
| **400** | Invalid input, or Meta rejected the image |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="uploadadvideo"></a>
# **UploadAdVideo**
> UploadAdVideo201Response UploadAdVideo (UploadAdVideoRequest uploadAdVideoRequest)

Upload an ad video

Standalone ad-video upload (parallel to POST /v1/ads/images), so a video creative can be rendered via POST /v1/ads/preview or attached via `video.id` on POST /v1/ads/create before an ad exists.  Accepts either an https `videoUrl` we download server-side (SSRF-guarded) or raw `videoBase64` bytes; exactly one is required. `videoBase64` is capped by Vercel's body limit — around 4.5 MB payload in practice, so larger videos must come via `videoUrl`.  Returns the Meta `video.id` (reusable wherever `video.id` is accepted) plus Meta's auto-generated poster URL when available. The endpoint waits until Meta reports the video ready (chunked upload + transcode can take minutes; the handler runs up to 800 s).

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
    public class UploadAdVideoExample
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
            var apiInstance = new AdCreativesApi(httpClient, config, httpClientHandler);
            var uploadAdVideoRequest = new UploadAdVideoRequest(); // UploadAdVideoRequest | 

            try
            {
                // Upload an ad video
                UploadAdVideo201Response result = apiInstance.UploadAdVideo(uploadAdVideoRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCreativesApi.UploadAdVideo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadAdVideoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload an ad video
    ApiResponse<UploadAdVideo201Response> response = apiInstance.UploadAdVideoWithHttpInfo(uploadAdVideoRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCreativesApi.UploadAdVideoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **uploadAdVideoRequest** | [**UploadAdVideoRequest**](UploadAdVideoRequest.md) |  |  |

### Return type

[**UploadAdVideo201Response**](UploadAdVideo201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Video uploaded and ready |  -  |
| **400** | Invalid input, or Meta rejected the upload |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no video id). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

