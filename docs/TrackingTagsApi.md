# Zernio.Api.TrackingTagsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddTrackingTagSharedAccount**](TrackingTagsApi.md#addtrackingtagsharedaccount) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Share with an ad account |
| [**CreateTrackingTag**](TrackingTagsApi.md#createtrackingtag) | **POST** /v1/accounts/{accountId}/tracking-tags | Create a tracking tag |
| [**CreateTrackingTagEvent**](TrackingTagsApi.md#createtrackingtagevent) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/events | Create a conversion event |
| [**DeleteTrackingTagEvent**](TrackingTagsApi.md#deletetrackingtagevent) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/events/{eventId} | Delete a conversion event |
| [**GetAdTrackingTags**](TrackingTagsApi.md#getadtrackingtags) | **GET** /v1/ads/{adId}/tracking-tags | Get ad tracking tags |
| [**GetTrackingTag**](TrackingTagsApi.md#gettrackingtag) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId} | Get a tracking tag |
| [**GetTrackingTagStats**](TrackingTagsApi.md#gettrackingtagstats) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/stats | Get aggregated event stats |
| [**GetTrackingTagStoreInstall**](TrackingTagsApi.md#gettrackingtagstoreinstall) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Get store install status |
| [**InstallTrackingTagOnStore**](TrackingTagsApi.md#installtrackingtagonstore) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Install on a Shopify store or WordPress site |
| [**ListTrackingTagEvents**](TrackingTagsApi.md#listtrackingtagevents) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/events | List conversion events |
| [**ListTrackingTagSharedAccounts**](TrackingTagsApi.md#listtrackingtagsharedaccounts) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | List accounts it is shared with |
| [**ListTrackingTags**](TrackingTagsApi.md#listtrackingtags) | **GET** /v1/accounts/{accountId}/tracking-tags | List tracking tags |
| [**RemoveTrackingTagFromStore**](TrackingTagsApi.md#removetrackingtagfromstore) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Remove from a Shopify store or WordPress site |
| [**RemoveTrackingTagSharedAccount**](TrackingTagsApi.md#removetrackingtagsharedaccount) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Stop sharing with an account |
| [**UpdateAdTrackingTags**](TrackingTagsApi.md#updateadtrackingtags) | **PATCH** /v1/ads/{adId}/tracking-tags | Set ad tracking tags |
| [**UpdateTrackingTag**](TrackingTagsApi.md#updatetrackingtag) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId} | Update a tracking tag |
| [**UpdateTrackingTagEvent**](TrackingTagsApi.md#updatetrackingtagevent) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId}/events/{eventId} | Update a conversion event |

<a id="addtrackingtagsharedaccount"></a>
# **AddTrackingTagSharedAccount**
> AddTrackingTagSharedAccount201Response AddTrackingTagSharedAccount (string accountId, string tagId, AddTrackingTagSharedAccountRequest addTrackingTagSharedAccountRequest)

Share with an ad account

Shares the pixel with another ad account so campaigns/audiences in that account can use it. Requires that you administer both the pixel's owning Business Manager and the target ad account; a pixel on a personal (non-BM) ad account can't be shared (Meta will reject the call). Meta only (platform `metaads`); other platforms return 501. 

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
    public class AddTrackingTagSharedAccountExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var addTrackingTagSharedAccountRequest = new AddTrackingTagSharedAccountRequest(); // AddTrackingTagSharedAccountRequest | 

            try
            {
                // Share with an ad account
                AddTrackingTagSharedAccount201Response result = apiInstance.AddTrackingTagSharedAccount(accountId, tagId, addTrackingTagSharedAccountRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.AddTrackingTagSharedAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddTrackingTagSharedAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Share with an ad account
    ApiResponse<AddTrackingTagSharedAccount201Response> response = apiInstance.AddTrackingTagSharedAccountWithHttpInfo(accountId, tagId, addTrackingTagSharedAccountRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.AddTrackingTagSharedAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **addTrackingTagSharedAccountRequest** | [**AddTrackingTagSharedAccountRequest**](AddTrackingTagSharedAccountRequest.md) |  |  |

### Return type

[**AddTrackingTagSharedAccount201Response**](AddTrackingTagSharedAccount201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Tracking tag shared with the ad account |  -  |
| **400** | Invalid body / &#x60;adAccountId&#x60;, or Meta rejected the share (e.g. personal ad account). |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtrackingtag"></a>
# **CreateTrackingTag**
> CreateTrackingTag201Response CreateTrackingTag (string accountId, CreateTrackingTagRequest createTrackingTagRequest)

Create a tracking tag

Meta: creates a Meta Pixel on the given ad account (`POST /act_{id}/adspixels`, where `name` is the only input). Returns the created tag including its install `code`. The pixel is owned by the Business Manager that owns the ad account; a pixel created on a personal (non-BM) ad account ends up with `ownerBusinessId: null` and can't be shared with other ad accounts.  Creating a Meta pixel does NOT install it. Install the returned `code` snippet on the site, or send events server-side via `POST /v1/ads/conversions`. The check `installed` is derived from `lastFiredTime`.  OpenAI Ads: creates an OpenAI pixel AND provisions a Conversions API key for it in the same call (`adAccountId` is required by this endpoint but ignored: one API key maps to exactly one ad account, so there's nothing to select). Returns 422 (`FEATURE_NOT_AVAILABLE`) if the ad account isn't enabled for pixel management; contact your OpenAI partner representative to enable it. There is no delete API for OpenAI pixels. If the pixel is created but the Conversions API key provisioning then fails, the pixel is left live on OpenAI (it cannot be cleaned up) and the error message names the surviving pixel id and warns against retrying, since a retry would create a second, orphaned pixel.  NOT idempotent on either platform: each call creates a new pixel (and, for OpenAI, a new Conversions API key plus, with `defaultEventType`, a new conversion event setting). Do not retry blindly on timeout. Meta (platform `metaads`) and OpenAI Ads (platform `openaiads`); other platforms return 501. 

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
    public class CreateTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Ads SocialAccount id (platform `metaads` or `openaiads`).
            var createTrackingTagRequest = new CreateTrackingTagRequest(); // CreateTrackingTagRequest | 

            try
            {
                // Create a tracking tag
                CreateTrackingTag201Response result = apiInstance.CreateTrackingTag(accountId, createTrackingTagRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a tracking tag
    ApiResponse<CreateTrackingTag201Response> response = apiInstance.CreateTrackingTagWithHttpInfo(accountId, createTrackingTagRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Ads SocialAccount id (platform &#x60;metaads&#x60; or &#x60;openaiads&#x60;). |  |
| **createTrackingTagRequest** | [**CreateTrackingTagRequest**](CreateTrackingTagRequest.md) |  |  |

### Return type

[**CreateTrackingTag201Response**](CreateTrackingTag201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Tracking tag created |  -  |
| **400** | Invalid body, invalid &#x60;adAccountId&#x60;, over the per-business pixel cap, or ad account not in a Business Manager. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | OpenAI Ads only: the ad account is not enabled for pixel management. Contact your OpenAI partner representative. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Creating a pixel is NOT idempotent, so before retrying confirm with GET /v1/accounts/{accountId}/tracking-tags that no pixel was created. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createtrackingtagevent"></a>
# **CreateTrackingTagEvent**
> CreateTrackingTagEvent201Response CreateTrackingTagEvent (string accountId, string tagId, CreateTrackingTagEventRequest createTrackingTagEventRequest)

Create a conversion event

Creates a conversion event tied to the tag. Pass the platform's own event type in `type` (e.g. Google `PURCHASE`, LinkedIn `ADD_TO_CART`, X `CHECKOUT_INITIATED`) or a neutral `siteEvent` the platform maps to its closest type. Each platform stores a subset of the optional fields; sending one it does not store answers 400 naming the supported fields. NOT idempotent unless noted per platform: do not retry blindly. 

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
    public class CreateTrackingTagEventExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var createTrackingTagEventRequest = new CreateTrackingTagEventRequest(); // CreateTrackingTagEventRequest | 

            try
            {
                // Create a conversion event
                CreateTrackingTagEvent201Response result = apiInstance.CreateTrackingTagEvent(accountId, tagId, createTrackingTagEventRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTagEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTrackingTagEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a conversion event
    ApiResponse<CreateTrackingTagEvent201Response> response = apiInstance.CreateTrackingTagEventWithHttpInfo(accountId, tagId, createTrackingTagEventRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.CreateTrackingTagEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **createTrackingTagEventRequest** | [**CreateTrackingTagEventRequest**](CreateTrackingTagEventRequest.md) |  |  |

### Return type

[**CreateTrackingTagEvent201Response**](CreateTrackingTagEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Conversion event created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform cannot create conversion events through its API (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletetrackingtagevent"></a>
# **DeleteTrackingTagEvent**
> DeleteTrackingTagEvent200Response DeleteTrackingTagEvent (string accountId, string tagId, string eventId, string? adAccountId = null)

Delete a conversion event

Removes the conversion event. Platforms without a hard delete archive or disable it instead; `state` in the response says which (`deleted`, `archived`, `disabled`). 

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
    public class DeleteTrackingTagEventExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | 
            var eventId = "eventId_example";  // string | Event id (`TrackingTagEvent.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // Delete a conversion event
                DeleteTrackingTagEvent200Response result = apiInstance.DeleteTrackingTagEvent(accountId, tagId, eventId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.DeleteTrackingTagEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTrackingTagEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a conversion event
    ApiResponse<DeleteTrackingTagEvent200Response> response = apiInstance.DeleteTrackingTagEventWithHttpInfo(accountId, tagId, eventId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.DeleteTrackingTagEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** |  |  |
| **eventId** | **string** | Event id (&#x60;TrackingTagEvent.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**DeleteTrackingTagEvent200Response**](DeleteTrackingTagEvent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversion event removed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform cannot remove conversion events through its API (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadtrackingtags"></a>
# **GetAdTrackingTags**
> GetAdTrackingTags200Response GetAdTrackingTags (string adId)

Get ad tracking tags

Unified read of the platform's native click-URL tracking params. - Meta (facebook/instagram): the creative's `url_tags` (and template_url_spec). - Google (googleads): the campaign's `trackingUrlTemplate` + `finalUrlSuffix`. - LinkedIn (linkedinads): the campaign's Dynamic UTM `dynamicValueParameters` + `customValueParameters`. Returns 405 for platforms without a click-URL tracking surface (TikTok, X, Pinterest).  **Not pixels.** Despite the shared path segment, this endpoint has nothing to do with measurement tags. For an ad account's pixels use `GET /v1/accounts/{accountId}/tracking-tags?adAccountId=act_...` (Meta Pixels, with `kind` and `ownerAdAccountId`) or `GET /v1/accounts/{accountId}/conversion-destinations`. 

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
    public class GetAdTrackingTagsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Ad id (hex _id, platformAdId, or effective story/media id).

            try
            {
                // Get ad tracking tags
                GetAdTrackingTags200Response result = apiInstance.GetAdTrackingTags(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetAdTrackingTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdTrackingTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ad tracking tags
    ApiResponse<GetAdTrackingTags200Response> response = apiInstance.GetAdTrackingTagsWithHttpInfo(adId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetAdTrackingTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Ad id (hex _id, platformAdId, or effective story/media id). |  |

### Return type

[**GetAdTrackingTags200Response**](GetAdTrackingTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tags for the ad&#39;s platform (shape varies by platform). |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad not found |  -  |
| **405** | Platform has no click-URL tracking surface |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtag"></a>
# **GetTrackingTag**
> GetTrackingTag200Response GetTrackingTag (string accountId, string tagId, string? adAccountId = null)

Get a tracking tag

Returns the full tag record including the base-code `code` snippet, `lastFiredTime`, `ownerBusinessId`, `isUnavailable`, etc. Meta only (platform `metaads`); other platforms return 501.  OpenAI Ads (`openaiads`): `tagId` is the pixel's API id (`cds_...`) or its `pixel_id`. OpenAI documents no single-pixel read, so the tag is resolved from the pixel list; the response adds `code` (the official `oaiq` base code plus `page_viewed`) and `events` (the conversion event settings whose source is this pixel). `siteTagId` is the `pixel_id` the site and the Conversions API send; `id` is what event settings reference. 

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
    public class GetTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. (optional) 

            try
            {
                // Get a tracking tag
                GetTrackingTag200Response result = apiInstance.GetTrackingTag(accountId, tagId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a tracking tag
    ApiResponse<GetTrackingTag200Response> response = apiInstance.GetTrackingTagWithHttpInfo(accountId, tagId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. | [optional]  |

### Return type

[**GetTrackingTag200Response**](GetTrackingTag200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tag fetched |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtagstats"></a>
# **GetTrackingTagStats**
> GetTrackingTagStats200Response GetTrackingTagStats (string accountId, string tagId, string? adAccountId = null, string? aggregation = null, int? startTime = null, int? endTime = null)

Get aggregated event stats

Returns event counts / health for the tag, where the platform exposes them. Meta: aggregated counts (`GET /{pixel_id}/stats`), rows passed through as-is; their shape depends on the `aggregation` requested. Platforms without a stats API answer 501.  OpenAI Ads: the recent-events stream (`GET /conversions/events`), the latest (at most 50) Pixel SDK events received in the last 15 minutes, one row per event (`event_type`, `api_channel`, `event_timestamp_ms`, `received_at_ms`, ...). Conversions API events are not included. It is a fixed window: `startTime`/`endTime` answer 400. Use it to confirm an install fires; attributed totals come from ads analytics. Accounts not enabled for the stream answer 422 `feature_not_available`. 

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
    public class GetTrackingTagStatsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. (optional) 
            var aggregation = "event";  // string? | Meta only (400 on other platforms): aggregation dimension. Defaults to `event`. (optional)  (default to event)
            var startTime = 56;  // int? | Unix seconds lower bound. (optional) 
            var endTime = 56;  // int? | Unix seconds upper bound. (optional) 

            try
            {
                // Get aggregated event stats
                GetTrackingTagStats200Response result = apiInstance.GetTrackingTagStats(accountId, tagId, adAccountId, aggregation, startTime, endTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get aggregated event stats
    ApiResponse<GetTrackingTagStats200Response> response = apiInstance.GetTrackingTagStatsWithHttpInfo(accountId, tagId, adAccountId, aggregation, startTime, endTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStatsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. | [optional]  |
| **aggregation** | **string?** | Meta only (400 on other platforms): aggregation dimension. Defaults to &#x60;event&#x60;. | [optional] [default to event] |
| **startTime** | **int?** | Unix seconds lower bound. | [optional]  |
| **endTime** | **int?** | Unix seconds upper bound. | [optional]  |

### Return type

[**GetTrackingTagStats200Response**](GetTrackingTagStats200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Stats fetched |  -  |
| **400** | Invalid query parameter. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="gettrackingtagstoreinstall"></a>
# **GetTrackingTagStoreInstall**
> GetTrackingTagStoreInstall200Response GetTrackingTagStoreInstall (string accountId, string tagId, string storeAccountId, string? adAccountId = null)

Get store install status

Whether this tag is the one the Shopify store fires for its platform. `installedTagId` names the tag of that platform the store currently fires, which can be a different tag, and `tags` lists every Zernio tag on the store (all platforms).  WordPress: whether the Zernio widget for this pixel is live (in an active widget area, script intact), plus a read-only `preflight` with the theme's widget areas and, when an install would be blocked, the `reason` POST would return. The preflight reads capabilities only, so `ready: true` is not a guarantee: `DISALLOW_UNFILTERED_HTML` or a multisite admin who is not a Super Admin still strips the script, which POST detects. `tags` lists every Zernio widget on the site (all platforms, with `active`). 

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
    public class GetTrackingTagStoreInstallExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var storeAccountId = "storeAccountId_example";  // string | The connected Shopify or WordPress account id.
            var adAccountId = "adAccountId_example";  // string? | Scopes the tag lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // Get store install status
                GetTrackingTagStoreInstall200Response result = apiInstance.GetTrackingTagStoreInstall(accountId, tagId, storeAccountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStoreInstall: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTrackingTagStoreInstallWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get store install status
    ApiResponse<GetTrackingTagStoreInstall200Response> response = apiInstance.GetTrackingTagStoreInstallWithHttpInfo(accountId, tagId, storeAccountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.GetTrackingTagStoreInstallWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **storeAccountId** | **string** | The connected Shopify or WordPress account id. |  |
| **adAccountId** | **string?** | Scopes the tag lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**GetTrackingTagStoreInstall200Response**](GetTrackingTagStoreInstall200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Install status |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The store must re-approve the Zernio Shopify app to grant pixel access (code &#x60;reconnect_required&#x60;). Send the merchant to &#x60;details.authUrl&#x60;; the Shopify account id stays the same. Also returned while the store account itself needs reconnection (code &#x60;ads_connection_required&#x60;). |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="installtrackingtagonstore"></a>
# **InstallTrackingTagOnStore**
> InstallTrackingTagOnStore200Response InstallTrackingTagOnStore (string accountId, string tagId, InstallTrackingTagOnStoreRequest installTrackingTagOnStoreRequest)

Install on a Shopify store or WordPress site

Puts the Meta pixel on a connected Shopify store's storefront and checkout through Zernio's Shopify web pixel (a Shopify app pixel, no theme edits). The store then sends PageView, ViewContent, AddToCart, Search, InitiateCheckout, AddPaymentInfo and Purchase (with value, currency, content_ids and contents) to the pixel, each with an event id. Purchase uses `shopify_order_{orderId}` as its event id, so a Conversions API Purchase you send for the same order with that `eventId` is deduplicated by Meta.  Idempotent: a store runs one Zernio web pixel holding one tag per platform, so calling it again updates the install, installing a different tag of the same platform replaces the previous one (reported in `replacedTagId`), and other platforms' tags are kept. Events respect the store's customer privacy settings (marketing consent).  `accountId` is the Meta ads account that owns the pixel (`tagId`); `storeAccountId` is the Shopify account.  OpenAI Ads on Shopify: each event is sent through OpenAI's documented image tag (`GET https://bzr.openai.com/v1/sdk/events`) as `page_viewed`, `contents_viewed`, `items_added`, `checkout_started`, `order_created`, and custom events `search` and `addpaymentinfo` (lowercase, so a Conversions API Search/AddPaymentInfo with the same event id deduplicates). Amounts are sent in the currency's minor unit. The landing page's `oppref` click id is kept in the `__oppref` cookie for 30 days and sent with every event. The image tag cannot carry the `__obref` browser id (OpenAI rejects the parameter), and the search text is never sent. On WordPress the widget holds the official `oaiq` base code and a `page_viewed` call.  Stores connected before pixel support must re-approve the Zernio app: the call then answers 409 `reconnect_required` with `details.authUrl` to send the merchant to (the Shopify account id stays the same). Platforms without an install path return 501.  **WordPress** (`storeAccountId` is a connected WordPress.com or self-hosted site): Zernio adds a Custom HTML widget with the Meta pixel base code (fbevents.js, `init`, `PageView`) to a widget area of the active theme (a footer area when there is one, else the first active area; pass `sidebarId` to choose), then reads the widget back to confirm WordPress kept the `<script>` tag. The widget carries a Zernio marker, so the call is idempotent per pixel: repeating it updates or moves the same widget, and pixel code the site owner pasted by hand is never touched. Several pixels can run side by side (one widget each). When the site cannot run the pixel, nothing is left behind and the call answers 422 `tracking_tag_install_blocked` with `details.reason`: - `insufficient_permissions`: the connected user lacks `edit_theme_options` (needs Administrator). - `scripts_stripped`: WordPress removed the script (the user lacks `unfiltered_html`, e.g. a multisite admin who is not a Super Admin, or `DISALLOW_UNFILTERED_HTML` is set). - `wordpress_com_plan`: a WordPress.com plan that strips scripts (plans without plugins). - `no_widget_areas`: the theme has no widget areas (block themes such as Twenty Twenty-Five). - `widgets_api_unavailable`: no widgets REST API (WordPress older than 5.8, or disabled). The `error` message names the manual alternative (Meta's official WordPress plugin). With `verifyHomepage` (default true) the homepage is fetched afterwards and `homepageCheck` says whether the pixel is visible; `not_found` can be a stale page cache, the widget read-back is authoritative. 

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
    public class InstallTrackingTagOnStoreExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var installTrackingTagOnStoreRequest = new InstallTrackingTagOnStoreRequest(); // InstallTrackingTagOnStoreRequest | 

            try
            {
                // Install on a Shopify store or WordPress site
                InstallTrackingTagOnStore200Response result = apiInstance.InstallTrackingTagOnStore(accountId, tagId, installTrackingTagOnStoreRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.InstallTrackingTagOnStore: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the InstallTrackingTagOnStoreWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Install on a Shopify store or WordPress site
    ApiResponse<InstallTrackingTagOnStore200Response> response = apiInstance.InstallTrackingTagOnStoreWithHttpInfo(accountId, tagId, installTrackingTagOnStoreRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.InstallTrackingTagOnStoreWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **installTrackingTagOnStoreRequest** | [**InstallTrackingTagOnStoreRequest**](InstallTrackingTagOnStoreRequest.md) |  |  |

### Return type

[**InstallTrackingTagOnStore200Response**](InstallTrackingTagOnStore200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pixel installed on the store |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The store must re-approve the Zernio Shopify app to grant pixel access (code &#x60;reconnect_required&#x60;). Send the merchant to &#x60;details.authUrl&#x60;; the Shopify account id stays the same. Also returned while the store account itself needs reconnection (code &#x60;ads_connection_required&#x60;). |  -  |
| **422** | WordPress only: the site cannot run the pixel and nothing was left on it. Code &#x60;tracking_tag_install_blocked&#x60;; the reason is in &#x60;details.reason&#x60;. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta, Shopify or the WordPress site was unreachable or returned an unclassified error. On WordPress a write may have completed; call GET before retrying. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtagevents"></a>
# **ListTrackingTagEvents**
> ListTrackingTagEvents200Response ListTrackingTagEvents (string accountId, string tagId, string? adAccountId = null)

List conversion events

The tag's conversion events, on platforms where each conversion is its own object: Google conversion actions, LinkedIn conversion rules, X web event tags, OpenAI event settings, TikTok pixel events, Meta custom conversions. Platforms where events are just names the site sends (Pinterest) answer 501. 

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
    public class ListTrackingTagEventsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var adAccountId = "adAccountId_example";  // string? | Scopes the lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // List conversion events
                ListTrackingTagEvents200Response result = apiInstance.ListTrackingTagEvents(accountId, tagId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List conversion events
    ApiResponse<ListTrackingTagEvents200Response> response = apiInstance.ListTrackingTagEventsWithHttpInfo(accountId, tagId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **adAccountId** | **string?** | Scopes the lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**ListTrackingTagEvents200Response**](ListTrackingTagEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversion events listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform has no conversion-event objects (code &#x60;platform_not_supported&#x60;); the message names the alternative. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtagsharedaccounts"></a>
# **ListTrackingTagSharedAccounts**
> ListTrackingTagSharedAccounts200Response ListTrackingTagSharedAccounts (string accountId, string tagId)

List accounts it is shared with

Meta only (platform `metaads`); other platforms return 501.

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
    public class ListTrackingTagSharedAccountsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.

            try
            {
                // List accounts it is shared with
                ListTrackingTagSharedAccounts200Response result = apiInstance.ListTrackingTagSharedAccounts(accountId, tagId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagSharedAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagSharedAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List accounts it is shared with
    ApiResponse<ListTrackingTagSharedAccounts200Response> response = apiInstance.ListTrackingTagSharedAccountsWithHttpInfo(accountId, tagId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagSharedAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |

### Return type

[**ListTrackingTagSharedAccounts200Response**](ListTrackingTagSharedAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shared ad accounts listed |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtrackingtags"></a>
# **ListTrackingTags**
> ListTrackingTags200Response ListTrackingTags (string accountId, string? adAccountId = null)

List tracking tags

Returns the tracking tags (Meta Pixels, or OpenAI Ads pixels) the connected ads account can see. Pass `?adAccountId=act_...` (Meta only) to scope the list to a single ad account; omit it to list every pixel reachable by the token (the name is then suffixed with the ad account it was discovered on, for disambiguation). The list view omits `code`. Call `getTrackingTag` for the install snippet and full detail.  Meta (platform `metaads`) and OpenAI Ads (platform `openaiads`); other platforms return 501. The `accountId` must be the ads SocialAccount created by the Ads add-on connect flow (Meta) or the OpenAI Ads connect flow, not a Facebook/Instagram posting account. Get your Meta `act_...` ids from `GET /v1/ads/accounts`; `adAccountId` is ignored for OpenAI Ads (one API key maps to exactly one ad account). 

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
    public class ListTrackingTagsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Ads SocialAccount id (platform `metaads` or `openaiads`).
            var adAccountId = "adAccountId_example";  // string? | Optional, Meta only. Scope to one ad account, e.g. `act_123456789`. Ignored for OpenAI Ads. (optional) 

            try
            {
                // List tracking tags
                ListTrackingTags200Response result = apiInstance.ListTrackingTags(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTrackingTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List tracking tags
    ApiResponse<ListTrackingTags200Response> response = apiInstance.ListTrackingTagsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.ListTrackingTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Ads SocialAccount id (platform &#x60;metaads&#x60; or &#x60;openaiads&#x60;). |  |
| **adAccountId** | **string?** | Optional, Meta only. Scope to one ad account, e.g. &#x60;act_123456789&#x60;. Ignored for OpenAI Ads. | [optional]  |

### Return type

[**ListTrackingTags200Response**](ListTrackingTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tags listed |  -  |
| **400** | Account platform not supported, or invalid &#x60;adAccountId&#x60;. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removetrackingtagfromstore"></a>
# **RemoveTrackingTagFromStore**
> RemoveTrackingTagFromStore200Response RemoveTrackingTagFromStore (string accountId, string tagId, string storeAccountId, string? adAccountId = null)

Remove from a Shopify store or WordPress site

Removes the tag from the store. Idempotent: nothing installed returns 200 with `installed: false`. If the store fires a different tag of the same platform, nothing is removed and the call answers 409 `invalid_resource_state`. Shopify: other platforms' tags stay; the web pixel itself is deleted once no tag remains.  WordPress: deletes every widget Zernio created for this pixel and reports how many in `removed` (0 when nothing was installed). Pixel code added by hand is left alone. 

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
    public class RemoveTrackingTagFromStoreExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Tag id (`TrackingTag.id`).
            var storeAccountId = "storeAccountId_example";  // string | The connected Shopify or WordPress account id.
            var adAccountId = "adAccountId_example";  // string? | Scopes the tag lookup on platforms whose tag ids live inside an ad account. (optional) 

            try
            {
                // Remove from a Shopify store or WordPress site
                RemoveTrackingTagFromStore200Response result = apiInstance.RemoveTrackingTagFromStore(accountId, tagId, storeAccountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagFromStore: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveTrackingTagFromStoreWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove from a Shopify store or WordPress site
    ApiResponse<RemoveTrackingTagFromStore200Response> response = apiInstance.RemoveTrackingTagFromStoreWithHttpInfo(accountId, tagId, storeAccountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagFromStoreWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Tag id (&#x60;TrackingTag.id&#x60;). |  |
| **storeAccountId** | **string** | The connected Shopify or WordPress account id. |  |
| **adAccountId** | **string?** | Scopes the tag lookup on platforms whose tag ids live inside an ad account. | [optional]  |

### Return type

[**RemoveTrackingTagFromStore200Response**](RemoveTrackingTagFromStore200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pixel removed (or was not installed) |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The store fires a different pixel (code &#x60;invalid_resource_state&#x60;), or the store must re-approve the Zernio app (code &#x60;reconnect_required&#x60;, see &#x60;details.authUrl&#x60;). |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removetrackingtagsharedaccount"></a>
# **RemoveTrackingTagSharedAccount**
> void RemoveTrackingTagSharedAccount (string accountId, string tagId, string? adAccountId = null)

Stop sharing with an account

`adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. Meta only (platform `metaads`); other platforms return 501. 

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
    public class RemoveTrackingTagSharedAccountExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var adAccountId = "adAccountId_example";  // string? | Ad account to unshare, e.g. `act_123456789`. May also be sent in the JSON body. (optional) 

            try
            {
                // Stop sharing with an account
                apiInstance.RemoveTrackingTagSharedAccount(accountId, tagId, adAccountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagSharedAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveTrackingTagSharedAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Stop sharing with an account
    apiInstance.RemoveTrackingTagSharedAccountWithHttpInfo(accountId, tagId, adAccountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.RemoveTrackingTagSharedAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **adAccountId** | **string?** | Ad account to unshare, e.g. &#x60;act_123456789&#x60;. May also be sent in the JSON body. | [optional]  |

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
| **204** | Ad account unshared (no content). |  -  |
| **400** | &#x60;adAccountId&#x60; missing (neither query nor body), or Meta rejected the unshare. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadtrackingtags"></a>
# **UpdateAdTrackingTags**
> UpdateAdTrackingTags200Response UpdateAdTrackingTags (string adId, UpdateAdTrackingTagsRequest updateAdTrackingTagsRequest)

Set ad tracking tags

Unified update. Send only the fields for the ad's platform: - Meta: `urlTags` (array of {key,value}). Meta creatives are immutable, so this rebuilds the   creative and repoints the ad. By DEFAULT we PRESERVE the existing creative verbatim   (re-post its object_story_spec + the new url_tags, reusing the image), so you send `urlTags`   ALONE, with no need to read back headline/body/CTA. `creative` (headline, body, callToAction,   linkUrl, imageUrl) is OPTIONAL and only needed to rebuild explicitly, or for SHARE / page-post   / dark / asset_feed creatives whose object_story_spec Meta strips (those return 422 asking for   `creative`). - Google: `trackingUrlTemplate` and/or `finalUrlSuffix` (full template strings; account quota applies). - LinkedIn: `dynamicValueParameters` and/or `customValueParameters` (campaign-level Dynamic UTM). 

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
    public class UpdateAdTrackingTagsExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 
            var updateAdTrackingTagsRequest = new UpdateAdTrackingTagsRequest(); // UpdateAdTrackingTagsRequest | 

            try
            {
                // Set ad tracking tags
                UpdateAdTrackingTags200Response result = apiInstance.UpdateAdTrackingTags(adId, updateAdTrackingTagsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.UpdateAdTrackingTags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdTrackingTagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set ad tracking tags
    ApiResponse<UpdateAdTrackingTags200Response> response = apiInstance.UpdateAdTrackingTagsWithHttpInfo(adId, updateAdTrackingTagsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.UpdateAdTrackingTagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** |  |  |
| **updateAdTrackingTagsRequest** | [**UpdateAdTrackingTagsRequest**](UpdateAdTrackingTagsRequest.md) |  |  |

### Return type

[**UpdateAdTrackingTags200Response**](UpdateAdTrackingTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tags as they now stand, in the same shape the GET on this path returns: &#x60;platform&#x60; plus the fields that platform supports. Meta returns &#x60;level&#x60;, &#x60;urlTags&#x60; and &#x60;templateUrlSpec&#x60;; Google returns &#x60;trackingUrlTemplate&#x60; and &#x60;finalUrlSuffix&#x60;. A field the platform does not support is absent.  |  -  |
| **401** | Unauthorized |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Ad not found |  -  |
| **405** | Platform has no click-URL tracking surface |  -  |
| **422** | Meta creative cannot be rebuilt (e.g. placement-customized/asset-feed/dark creative) |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetrackingtag"></a>
# **UpdateTrackingTag**
> GetTrackingTag200Response UpdateTrackingTag (string accountId, string tagId, UpdateTrackingTagRequest updateTrackingTagRequest)

Update a tracking tag

Partial-update a pixel. Whitelisted fields: `name` (rename), `enableAutomaticMatching`, `automaticMatchingFields`, `firstPartyCookieStatus`, `dataUseSetting`. At least one is required. Returns the re-fetched canonical tag. Meta only (platform `metaads`); other platforms return 501.  OpenAI Ads answers 501: its API has no pixel update or delete route (`POST`/`PATCH`/`PUT`/`DELETE /v1/conversions/pixels/{id}` answer 405 \"Invalid method\"); rename a pixel in OpenAI Ads Manager.  There is no DELETE: Meta has no API to delete a pixel. To stop using one, unshare it from your ad accounts (`DELETE .../tracking-tags/{tagId}/shared-accounts`) or disable it in Events Manager. 

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
    public class UpdateTrackingTagExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | Pixel id.
            var updateTrackingTagRequest = new UpdateTrackingTagRequest(); // UpdateTrackingTagRequest | 

            try
            {
                // Update a tracking tag
                GetTrackingTag200Response result = apiInstance.UpdateTrackingTag(accountId, tagId, updateTrackingTagRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrackingTagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a tracking tag
    ApiResponse<GetTrackingTag200Response> response = apiInstance.UpdateTrackingTagWithHttpInfo(accountId, tagId, updateTrackingTagRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** | Pixel id. |  |
| **updateTrackingTagRequest** | [**UpdateTrackingTagRequest**](UpdateTrackingTagRequest.md) |  |  |

### Return type

[**GetTrackingTag200Response**](GetTrackingTag200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tracking tag updated (re-fetched canonical state) |  -  |
| **400** | Invalid body (e.g. no fields supplied) or Meta validation failure. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the Meta token lacks ads permissions (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform does not offer this operation (code &#x60;platform_not_supported&#x60;); the message names the reason and the alternative. |  -  |
| **502** | Meta was unreachable or returned an unclassified error (type: platform_error; the raw Meta payload is in platformError). Retryable. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatetrackingtagevent"></a>
# **UpdateTrackingTagEvent**
> CreateTrackingTagEvent201Response UpdateTrackingTagEvent (string accountId, string tagId, string eventId, TrackingTagEventInput trackingTagEventInput)

Update a conversion event

Partial update; at least one field. A field the platform does not store answers 400.

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
    public class UpdateTrackingTagEventExample
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
            var apiInstance = new TrackingTagsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var tagId = "tagId_example";  // string | 
            var eventId = "eventId_example";  // string | Event id (`TrackingTagEvent.id`).
            var trackingTagEventInput = new TrackingTagEventInput(); // TrackingTagEventInput | 

            try
            {
                // Update a conversion event
                CreateTrackingTagEvent201Response result = apiInstance.UpdateTrackingTagEvent(accountId, tagId, eventId, trackingTagEventInput);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTagEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTrackingTagEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a conversion event
    ApiResponse<CreateTrackingTagEvent201Response> response = apiInstance.UpdateTrackingTagEventWithHttpInfo(accountId, tagId, eventId, trackingTagEventInput);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TrackingTagsApi.UpdateTrackingTagEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **tagId** | **string** |  |  |
| **eventId** | **string** | Event id (&#x60;TrackingTagEvent.id&#x60;). |  |
| **trackingTagEventInput** | [**TrackingTagEventInput**](TrackingTagEventInput.md) |  |  |

### Return type

[**CreateTrackingTagEvent201Response**](CreateTrackingTagEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversion event updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required, or the platform token lacks the permission (reconnect required). |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | The platform cannot update conversion events through its API (code &#x60;platform_not_supported&#x60;). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

