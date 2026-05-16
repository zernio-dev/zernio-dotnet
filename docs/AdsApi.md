# Zernio.Api.AdsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddConversionAssociations**](AdsApi.md#addconversionassociations) | **POST** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Associate campaigns with a conversion destination |
| [**BoostPost**](AdsApi.md#boostpost) | **POST** /v1/ads/boost | Boost post as ad |
| [**CreateConversionDestination**](AdsApi.md#createconversiondestination) | **POST** /v1/accounts/{accountId}/conversion-destinations | Create a conversion destination (LinkedIn) |
| [**CreateCtwaAd**](AdsApi.md#createctwaad) | **POST** /v1/ads/ctwa | Create Click-to-WhatsApp ad(s) |
| [**CreateStandaloneAd**](AdsApi.md#createstandalonead) | **POST** /v1/ads/create | Create standalone ad |
| [**DeleteAd**](AdsApi.md#deletead) | **DELETE** /v1/ads/{adId} | Cancel an ad |
| [**DeleteConversionDestination**](AdsApi.md#deleteconversiondestination) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Soft-delete a conversion destination |
| [**GetAd**](AdsApi.md#getad) | **GET** /v1/ads/{adId} | Get ad details |
| [**GetAdAnalytics**](AdsApi.md#getadanalytics) | **GET** /v1/ads/{adId}/analytics | Get ad analytics |
| [**GetAdComments**](AdsApi.md#getadcomments) | **GET** /v1/ads/{adId}/comments | List comments on an ad |
| [**GetConversionDestination**](AdsApi.md#getconversiondestination) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Fetch a single conversion destination |
| [**GetConversionMetrics**](AdsApi.md#getconversionmetrics) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/metrics | Fetch attribution metrics for a conversion destination |
| [**ListAdAccounts**](AdsApi.md#listadaccounts) | **GET** /v1/ads/accounts | List ad accounts |
| [**ListAds**](AdsApi.md#listads) | **GET** /v1/ads | List ads |
| [**ListAdsBusinessCenters**](AdsApi.md#listadsbusinesscenters) | **GET** /v1/ads/business-centers | List TikTok Business Centers |
| [**ListConversionAssociations**](AdsApi.md#listconversionassociations) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | List campaigns associated with a conversion destination |
| [**ListConversionDestinations**](AdsApi.md#listconversiondestinations) | **GET** /v1/accounts/{accountId}/conversion-destinations | List destinations for the Conversions API |
| [**RemoveConversionAssociations**](AdsApi.md#removeconversionassociations) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Remove campaign↔conversion associations |
| [**SearchAdInterests**](AdsApi.md#searchadinterests) | **GET** /v1/ads/interests | Search targeting interests |
| [**SearchAdTargetingLocations**](AdsApi.md#searchadtargetinglocations) | **GET** /v1/ads/targeting/search | Search geo targeting locations (Meta) |
| [**SendConversions**](AdsApi.md#sendconversions) | **POST** /v1/ads/conversions | Send conversion events to an ad platform |
| [**SendWhatsAppConversion**](AdsApi.md#sendwhatsappconversion) | **POST** /v1/whatsapp/conversions | Send WhatsApp conversion event |
| [**UpdateAd**](AdsApi.md#updatead) | **PUT** /v1/ads/{adId} | Update ad |
| [**UpdateConversionDestination**](AdsApi.md#updateconversiondestination) | **PATCH** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Update a conversion destination |

<a id="addconversionassociations"></a>
# **AddConversionAssociations**
> AddConversionAssociations200Response AddConversionAssociations (string accountId, string destinationId, AddConversionAssociationsRequest addConversionAssociationsRequest)

Associate campaigns with a conversion destination

Associate one or more campaigns with this conversion rule. Returns a per-campaign success/failure result so callers can retry only the rows that failed (e.g. wrong campaign type for the rule's objective). 

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
    public class AddConversionAssociationsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var addConversionAssociationsRequest = new AddConversionAssociationsRequest(); // AddConversionAssociationsRequest | 

            try
            {
                // Associate campaigns with a conversion destination
                AddConversionAssociations200Response result = apiInstance.AddConversionAssociations(accountId, destinationId, addConversionAssociationsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.AddConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Associate campaigns with a conversion destination
    ApiResponse<AddConversionAssociations200Response> response = apiInstance.AddConversionAssociationsWithHttpInfo(accountId, destinationId, addConversionAssociationsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.AddConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **addConversionAssociationsRequest** | [**AddConversionAssociationsRequest**](AddConversionAssociationsRequest.md) |  |  |

### Return type

[**AddConversionAssociations200Response**](AddConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-campaign batch result. Status is 200 even when some rows failed — inspect &#x60;failed[]&#x60; for details. Inputs that fail local URN validation are bucketed into &#x60;failed&#x60; without ever hitting LinkedIn.  |  -  |
| **400** | Invalid body. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | Account or destination not found. |  -  |
| **405** | Platform does not support associations. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="boostpost"></a>
# **BoostPost**
> UpdateAd200Response BoostPost (BoostPostRequest boostPostRequest)

Boost post as ad

Creates a paid ad campaign from an existing published post. Creates the full platform campaign hierarchy (campaign, ad set, ad).

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
    public class BoostPostExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var boostPostRequest = new BoostPostRequest(); // BoostPostRequest | 

            try
            {
                // Boost post as ad
                UpdateAd200Response result = apiInstance.BoostPost(boostPostRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.BoostPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BoostPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Boost post as ad
    ApiResponse<UpdateAd200Response> response = apiInstance.BoostPostWithHttpInfo(boostPostRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.BoostPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **boostPostRequest** | [**BoostPostRequest**](BoostPostRequest.md) |  |  |

### Return type

[**UpdateAd200Response**](UpdateAd200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Ad created |  -  |
| **400** | Missing required fields or invalid values |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads), missing linked account, or — for TikTok — the connected TikTok user is not authorized as an Identity on the target advertiser. Returned with code &#x60;ads_connection_required&#x60;; the message includes the actionable \&quot;TikTok Ads Manager → Assets → Identity\&quot; remediation step.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createconversiondestination"></a>
# **CreateConversionDestination**
> CreateConversionDestination201Response CreateConversionDestination (string accountId, CreateConversionDestinationRequest createConversionDestinationRequest)

Create a conversion destination (LinkedIn)

Create a new conversion rule on the platform. LinkedIn-only today; other platforms manage destinations in their own UIs and return 405.  For LinkedIn, the rule is created with `conversionMethod=CONVERSIONS_API` and (by default) auto-associated with all of the ad account's campaigns via `autoAssociationType=ALL_CAMPAIGNS`. Pass `autoAssociationType: NONE` to opt out and manage associations explicitly via the associations endpoints below.  365-day attribution windows are only valid for `SUBMIT_APPLICATION`, `PURCHASE`, `ADD_TO_CART`, `QUALIFIED_LEAD`, and `LEAD` rule types; the API rejects other combinations locally. 

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
    public class CreateConversionDestinationExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | SocialAccount ID (linkedinads).
            var createConversionDestinationRequest = new CreateConversionDestinationRequest(); // CreateConversionDestinationRequest | 

            try
            {
                // Create a conversion destination (LinkedIn)
                CreateConversionDestination201Response result = apiInstance.CreateConversionDestination(accountId, createConversionDestinationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.CreateConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a conversion destination (LinkedIn)
    ApiResponse<CreateConversionDestination201Response> response = apiInstance.CreateConversionDestinationWithHttpInfo(accountId, createConversionDestinationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.CreateConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | SocialAccount ID (linkedinads). |  |
| **createConversionDestinationRequest** | [**CreateConversionDestinationRequest**](CreateConversionDestinationRequest.md) |  |  |

### Return type

[**CreateConversionDestination201Response**](CreateConversionDestination201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Destination created |  -  |
| **400** | Invalid body or LinkedIn validation failure. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), or the connected LinkedIn account lacks the &#x60;rw_conversions&#x60; scope (reconnect required).  |  -  |
| **404** | Account not found or not accessible. |  -  |
| **405** | Platform does not support destination creation. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createctwaad"></a>
# **CreateCtwaAd**
> CreateCtwaAd201Response CreateCtwaAd (CreateCtwaAdRequest createCtwaAdRequest)

Create Click-to-WhatsApp ad(s)

Creates one or more Click-to-WhatsApp (CTWA) ads on Meta under a single campaign and ad set. When tapped, each ad opens a WhatsApp conversation with the business attached to the supplied Facebook Page. The full hierarchy (campaign, ad set, creative(s), ad(s)) is created and activated in one call. The CTA is locked to WHATSAPP_MESSAGE and the destination is hard-coded to api.whatsapp.com/send; Meta resolves the actual WhatsApp number from the Page-to-WA pairing configured in Page settings or Business Manager.  Supports two mutually-exclusive shapes:  - **Single-creative**: supply top-level `headline`, `body`, and one of   `imageUrl` / `video`. Creates 1 campaign + 1 ad set + 1 ad.  - **Multi-creative**: supply a `creatives[]` array with N entries   (each carrying its own headline, body, and image/video). Creates   1 campaign + 1 ad set + N ads sharing budget and targeting so Meta   A/Bs the creatives inside a single auction instead of fragmenting   budget across N parallel campaigns. Recommended when launching   multiple creative variants for the same campaign.   Prerequisites enforced by Meta (surfaced as platform_error on failure): the Facebook Page must be paired with a verified WhatsApp Business number, the WhatsApp Business Account must be business-verified, and the Meta access token must carry ads_management.

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
    public class CreateCtwaAdExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var createCtwaAdRequest = new CreateCtwaAdRequest(); // CreateCtwaAdRequest | 

            try
            {
                // Create Click-to-WhatsApp ad(s)
                CreateCtwaAd201Response result = apiInstance.CreateCtwaAd(createCtwaAdRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.CreateCtwaAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCtwaAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Click-to-WhatsApp ad(s)
    ApiResponse<CreateCtwaAd201Response> response = apiInstance.CreateCtwaAdWithHttpInfo(createCtwaAdRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.CreateCtwaAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCtwaAdRequest** | [**CreateCtwaAdRequest**](CreateCtwaAdRequest.md) |  |  |

### Return type

[**CreateCtwaAd201Response**](CreateCtwaAd201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | CTWA ad(s) created and submitted to Meta for review. Response is a tagged union discriminated by &#x60;adType&#x60;:  - &#x60;adType: \&quot;single\&quot;&#x60; → single-creative request: &#x60;{ adType, ad,   message }&#x60; where &#x60;ad&#x60; is the persisted Ad document. - &#x60;adType: \&quot;multi\&quot;&#x60; → multi-creative request: &#x60;{ adType, ads,   platformCampaignId, platformAdSetId, message }&#x60; where &#x60;ads&#x60; is   the array of N persisted Ad documents all sharing the returned   campaign and ad set IDs.  Generated SDK clients can narrow on &#x60;adType&#x60; instead of sniffing for field presence.  |  -  |
| **400** | Invalid body. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | SocialAccount not found. |  -  |
| **422** | Page is not connected to a verified WhatsApp number. |  -  |
| **502** | Meta rejected the request (e.g. WABA business verification missing). Inspect &#x60;platformError&#x60; for the upstream Meta payload.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createstandalonead"></a>
# **CreateStandaloneAd**
> CreateStandaloneAd201Response CreateStandaloneAd (CreateStandaloneAdRequest createStandaloneAdRequest)

Create standalone ad

Creates a paid ad with custom creative across Meta, Google Ads, Pinterest, TikTok, X/Twitter, and LinkedIn. Supports three mutually-exclusive request shapes selected by the body, a legacy single-creative shape (all platforms, default), a Meta-only multi-creative shape via the creatives array (one ad set with N ads sharing budget and targeting), and a Meta-only attach shape via adSetId (adds one new ad to an existing ad set). Per-platform required fields, budget minimums, and video-ad rules are documented on each property below. LinkedIn creates a Single Image or Single Video Ad backed by a Direct Sponsored Content \"dark post\" authored by a Company Page (see `organizationId`); supported goals are engagement, traffic, awareness, and video_views (video ads use the `video` field; video_views requires a video), and traffic ads require `linkUrl`.

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
    public class CreateStandaloneAdExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var createStandaloneAdRequest = new CreateStandaloneAdRequest(); // CreateStandaloneAdRequest | 

            try
            {
                // Create standalone ad
                CreateStandaloneAd201Response result = apiInstance.CreateStandaloneAd(createStandaloneAdRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.CreateStandaloneAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStandaloneAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create standalone ad
    ApiResponse<CreateStandaloneAd201Response> response = apiInstance.CreateStandaloneAdWithHttpInfo(createStandaloneAdRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.CreateStandaloneAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createStandaloneAdRequest** | [**CreateStandaloneAdRequest**](CreateStandaloneAdRequest.md) |  |  |

### Return type

[**CreateStandaloneAd201Response**](CreateStandaloneAd201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Ad(s) created |  -  |
| **400** | Missing required fields, invalid values, or non-Meta platform used with creatives[] / adSetId |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads) or missing linked account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletead"></a>
# **DeleteAd**
> DeleteAccountGroup200Response DeleteAd (string adId)

Cancel an ad

Cancels the ad on the platform and marks it as cancelled in the database. The ad is preserved for history.

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
    public class DeleteAdExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 

            try
            {
                // Cancel an ad
                DeleteAccountGroup200Response result = apiInstance.DeleteAd(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.DeleteAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel an ad
    ApiResponse<DeleteAccountGroup200Response> response = apiInstance.DeleteAdWithHttpInfo(adId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.DeleteAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** |  |  |

### Return type

[**DeleteAccountGroup200Response**](DeleteAccountGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad cancelled |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteconversiondestination"></a>
# **DeleteConversionDestination**
> void DeleteConversionDestination (string accountId, string destinationId, string? adAccountId = null)

Soft-delete a conversion destination

LinkedIn-only today. LinkedIn does not expose hard-delete on conversion rules — what their UI calls \"delete\" is the same `enabled: false` flip we apply here. The rule remains fetchable via GET with `status: 'inactive'`; the unified discovery endpoint hides it by default.  `adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. 

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
    public class DeleteConversionDestinationExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string? | Required as query OR in JSON body. (optional) 

            try
            {
                // Soft-delete a conversion destination
                apiInstance.DeleteConversionDestination(accountId, destinationId, adAccountId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.DeleteConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Soft-delete a conversion destination
    apiInstance.DeleteConversionDestinationWithHttpInfo(accountId, destinationId, adAccountId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.DeleteConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string?** | Required as query OR in JSON body. | [optional]  |

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
| **204** | Soft-deleted. |  -  |
| **400** | adAccountId missing. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | Account or destination not found. |  -  |
| **405** | Platform does not support deleting destinations. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getad"></a>
# **GetAd**
> GetAd200Response GetAd (string adId)

Get ad details

Returns an ad with its creative, targeting, status, and performance metrics.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: - the Zernio internal `_id` (24-char hex) - Meta's numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`) - the creative's `effective_object_story_id` (`{pageId}_{postId}` shape, Facebook side) - the creative's `effective_instagram_media_id` (Instagram side)  Any of the four resolve to the same ad. Caller doesn't need a translation step. 

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
    public class GetAdExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Zernio `_id` (hex), Meta `platformAdId` (numeric), or one of the creative's effective story/media IDs. See description for details. 

            try
            {
                // Get ad details
                GetAd200Response result = apiInstance.GetAd(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.GetAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ad details
    ApiResponse<GetAd200Response> response = apiInstance.GetAdWithHttpInfo(adId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.GetAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Zernio &#x60;_id&#x60; (hex), Meta &#x60;platformAdId&#x60; (numeric), or one of the creative&#39;s effective story/media IDs. See description for details.  |  |

### Return type

[**GetAd200Response**](GetAd200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadanalytics"></a>
# **GetAdAnalytics**
> GetAdAnalytics200Response GetAdAnalytics (string adId, DateOnly? fromDate = null, DateOnly? toDate = null, string? breakdowns = null)

Get ad analytics

Returns detailed performance analytics for an ad. Includes summary metrics, a daily timeline over the requested date range, and optional demographic breakdowns (Meta and TikTok only). If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max. 

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
    public class GetAdAnalyticsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 
            var breakdowns = "breakdowns_example";  // string? | Comma-separated breakdown dimensions. Meta: age, gender, country, publisher_platform, device_platform, region. TikTok: gender, age, country_code, platform, ac, language. (optional) 

            try
            {
                // Get ad analytics
                GetAdAnalytics200Response result = apiInstance.GetAdAnalytics(adId, fromDate, toDate, breakdowns);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.GetAdAnalytics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdAnalyticsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ad analytics
    ApiResponse<GetAdAnalytics200Response> response = apiInstance.GetAdAnalyticsWithHttpInfo(adId, fromDate, toDate, breakdowns);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.GetAdAnalyticsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** |  |  |
| **fromDate** | **DateOnly?** | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |
| **breakdowns** | **string?** | Comma-separated breakdown dimensions. Meta: age, gender, country, publisher_platform, device_platform, region. TikTok: gender, age, country_code, platform, ac, language. | [optional]  |

### Return type

[**GetAdAnalytics200Response**](GetAdAnalytics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad analytics |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcomments"></a>
# **GetAdComments**
> GetAdComments200Response GetAdComments (string adId, string? placement = null, int? limit = null, string? cursor = null)

List comments on an ad

Returns comments on an ad's underlying creative post. Useful for moderating or analyzing engagement on dark posts (ad creatives that never went live organically), which the regular GET /v1/inbox/comments/{postId} endpoint cannot serve because dark posts are not in Zernio's post database.  An ad that runs on both Facebook feed and Instagram feed has two separate underlying posts with separate comment threads (the creative's effective_object_story_id and effective_instagram_media_id). Use the `placement` query param to pick one; with no param the Instagram side is returned when it exists, otherwise Facebook. The identifiers are read from the ad record (persisted during sync) with a Marketing-API fallback for ads that predate the field.  For Instagram-placed comments, the Instagram account that runs the ad must be connected to Zernio — those comments are read through that account's token. If no connected Instagram account on the profile can read the ad's media, the call returns ads_connection_required (the Facebook side, if any, is still readable via ?placement=facebook).  Meta-only. Other ad platforms (TikTok, LinkedIn, Pinterest, Google, X) do not expose a public per-ad comments API and return feature_not_available.  Requires the Ads add-on. Response shape matches GET /v1/inbox/comments/{postId}.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: Zernio internal `_id` (24-char hex), Meta's numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`), or the creative's `effective_object_story_id` / `effective_instagram_media_id`. Caller doesn't need a translation step. 

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
    public class GetAdCommentsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Internal Zernio ad ID (ObjectId).
            var placement = "facebook";  // string? | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. (optional) 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var cursor = "cursor_example";  // string? | Pagination cursor from a previous response. (optional) 

            try
            {
                // List comments on an ad
                GetAdComments200Response result = apiInstance.GetAdComments(adId, placement, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.GetAdComments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCommentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List comments on an ad
    ApiResponse<GetAdComments200Response> response = apiInstance.GetAdCommentsWithHttpInfo(adId, placement, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.GetAdCommentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Internal Zernio ad ID (ObjectId). |  |
| **placement** | **string?** | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. | [optional]  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **cursor** | **string?** | Pagination cursor from a previous response. | [optional]  |

### Return type

[**GetAdComments200Response**](GetAdComments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comments on the ad |  -  |
| **400** | Invalid ad ID format, or the ad&#39;s creative format does not expose a commentable underlying post (code ad_not_commentable).  |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (legacy plans need the Ads add-on; included by default on usage-based plans), or ad platform is not Meta (code feature_not_available). |  -  |
| **404** | Resource not found |  -  |
| **422** | Ads account token unavailable, or (for Instagram-placed ads) no connected Instagram account on the profile can read the ad&#39;s media (code ads_connection_required).  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconversiondestination"></a>
# **GetConversionDestination**
> CreateConversionDestination201Response GetConversionDestination (string accountId, string destinationId, string adAccountId)

Fetch a single conversion destination

LinkedIn-only today. Returns the full destination record for one conversion rule. The `adAccountId` query parameter is required because LinkedIn rules are scoped to a sponsored ad account. 

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
    public class GetConversionDestinationExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | Numeric ID or full `urn:li:sponsoredAccount:{id}` URN.

            try
            {
                // Fetch a single conversion destination
                CreateConversionDestination201Response result = apiInstance.GetConversionDestination(accountId, destinationId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.GetConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Fetch a single conversion destination
    ApiResponse<CreateConversionDestination201Response> response = apiInstance.GetConversionDestinationWithHttpInfo(accountId, destinationId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.GetConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** | Numeric ID or full &#x60;urn:li:sponsoredAccount:{id}&#x60; URN. |  |

### Return type

[**CreateConversionDestination201Response**](CreateConversionDestination201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destination fetched |  -  |
| **400** | Validation error. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | Account or destination not found. |  -  |
| **405** | Platform does not support fetching a single destination. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getconversionmetrics"></a>
# **GetConversionMetrics**
> GetConversionMetrics200Response GetConversionMetrics (string accountId, string destinationId, string adAccountId, string startDate, string? endDate = null, string? granularity = null)

Fetch attribution metrics for a conversion destination

LinkedIn-only today. Returns conversion-attribution metrics (`externalWebsiteConversions`, `externalWebsitePostClickConversions`, `externalWebsitePostViewConversions`, `conversionValueInLocalCurrency`, `qualifiedLeads`, `costInLocalCurrency`) bucketed by date.  Date-range constraints (passed through from LinkedIn): - `granularity=DAILY` is retained for ~6 months only - `granularity=ALL` with a range > 6 months auto-rounds to month boundaries - `granularity=MONTHLY`/`YEARLY` retains 24 months  Throttle: LinkedIn caps adAnalytics at 45M metric values per 5-minute window across the calling token. Single-rule queries are well within that limit; surfaces as 429 if hit. 

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
    public class GetConversionMetricsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 
            var startDate = "startDate_example";  // string | 
            var endDate = "endDate_example";  // string? |  (optional) 
            var granularity = "ALL";  // string? |  (optional)  (default to DAILY)

            try
            {
                // Fetch attribution metrics for a conversion destination
                GetConversionMetrics200Response result = apiInstance.GetConversionMetrics(accountId, destinationId, adAccountId, startDate, endDate, granularity);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.GetConversionMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetConversionMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Fetch attribution metrics for a conversion destination
    ApiResponse<GetConversionMetrics200Response> response = apiInstance.GetConversionMetricsWithHttpInfo(accountId, destinationId, adAccountId, startDate, endDate, granularity);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.GetConversionMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |
| **startDate** | **string** |  |  |
| **endDate** | **string?** |  | [optional]  |
| **granularity** | **string?** |  | [optional] [default to DAILY] |

### Return type

[**GetConversionMetrics200Response**](GetConversionMetrics200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Metrics rows |  -  |
| **400** | Validation error or invalid date range. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | Account or destination not found. |  -  |
| **405** | Platform does not support metrics readback. |  -  |
| **429** | LinkedIn analytics rate limit hit. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadaccounts"></a>
# **ListAdAccounts**
> ListAdAccounts200Response ListAdAccounts (string accountId, string? adAccountId = null, int? limit = null)

List ad accounts

Returns the platform ad accounts available for the given social account (e.g. Meta ad accounts, TikTok advertiser IDs, Google Ads customer IDs).  For TikTok agencies: enumerates every advertiser under every Business Center the token can read (paginated server-side), then chunks the lookup against TikTok's `/advertiser/info/` endpoint (which has a per-call cap of ≤100 IDs). Solo advertisers without a BC fall back to the OAuth-time `advertiser_ids` list. Cached for 1h on the SocialAccount; lazy-refreshed on first call after expiry. 

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
    public class ListAdAccountsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Social account ID
            var adAccountId = "adAccountId_example";  // string? | Filter response to a single platform ad account ID (e.g. `act_123` for Meta, advertiser_id for TikTok). Returns at most one item. (optional) 
            var limit = 56;  // int? | Clamp the returned `accounts[]` length. Useful for typeahead pickers on agency tokens with hundreds of advertisers. (optional) 

            try
            {
                // List ad accounts
                ListAdAccounts200Response result = apiInstance.ListAdAccounts(accountId, adAccountId, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.ListAdAccounts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdAccountsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ad accounts
    ApiResponse<ListAdAccounts200Response> response = apiInstance.ListAdAccountsWithHttpInfo(accountId, adAccountId, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.ListAdAccountsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Social account ID |  |
| **adAccountId** | **string?** | Filter response to a single platform ad account ID (e.g. &#x60;act_123&#x60; for Meta, advertiser_id for TikTok). Returns at most one item. | [optional]  |
| **limit** | **int?** | Clamp the returned &#x60;accounts[]&#x60; length. Useful for typeahead pickers on agency tokens with hundreds of advertisers. | [optional]  |

### Return type

[**ListAdAccounts200Response**](ListAdAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad accounts |  -  |
| **401** | Unauthorized |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads) or Instagram missing linked Facebook account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listads"></a>
# **ListAds**
> ListAds200Response ListAds (int? page = null, int? limit = null, string? source = null, AdStatus? status = null, string? platform = null, string? accountId = null, string? adAccountId = null, string? profileId = null, string? campaignId = null, string? platformAdId = null, string? effectiveObjectStoryId = null, string? effectiveInstagramMediaId = null, DateOnly? fromDate = null, DateOnly? toDate = null)

List ads

Returns a paginated list of ads with metrics computed over an optional date range. Use source=all to include externally-synced ads from platform ad managers. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max.  To find the Zernio ad behind a comment you see in Meta Business Manager, filter by platformAdId (the Meta ad ID), effectiveObjectStoryId (Facebook), or effectiveInstagramMediaId (Instagram) — those are the post/media the ad's engagement lives on, and are also returned on each ad's `creative` object. Then call GET /v1/ads/{adId}/comments with the returned ad id. 

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
    public class ListAdsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var page = 1;  // int? | Page number (1-based) (optional)  (default to 1)
            var limit = 50;  // int? |  (optional)  (default to 50)
            var source = "zernio";  // string? | all (default) = Zernio-created + platform-discovered ads. zernio = restrict to Zernio-created only. (optional)  (default to all)
            var status = new AdStatus?(); // AdStatus? |  (optional) 
            var platform = "facebook";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? | Social account ID (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var campaignId = "campaignId_example";  // string? | Platform campaign ID (filter ads within a campaign) (optional) 
            var platformAdId = "platformAdId_example";  // string? | Meta ad ID. Returns the ad with this platform-side ad ID. (optional) 
            var effectiveObjectStoryId = "effectiveObjectStoryId_example";  // string? | Facebook `{pageId}_{postId}` of the post the ad's engagement lives on (Meta `effective_object_story_id`). Use to map a Business-Manager-visible post back to the Zernio ad. (optional) 
            var effectiveInstagramMediaId = "effectiveInstagramMediaId_example";  // string? | Instagram media ID of the boosted post (Meta `effective_instagram_media_id`). Use to map a Business-Manager-visible IG post back to the Zernio ad. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 

            try
            {
                // List ads
                ListAds200Response result = apiInstance.ListAds(page, limit, source, status, platform, accountId, adAccountId, profileId, campaignId, platformAdId, effectiveObjectStoryId, effectiveInstagramMediaId, fromDate, toDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.ListAds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ads
    ApiResponse<ListAds200Response> response = apiInstance.ListAdsWithHttpInfo(page, limit, source, status, platform, accountId, adAccountId, profileId, campaignId, platformAdId, effectiveObjectStoryId, effectiveInstagramMediaId, fromDate, toDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.ListAdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int?** |  | [optional] [default to 50] |
| **source** | **string?** | all (default) &#x3D; Zernio-created + platform-discovered ads. zernio &#x3D; restrict to Zernio-created only. | [optional] [default to all] |
| **status** | [**AdStatus?**](AdStatus?.md) |  | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **accountId** | **string?** | Social account ID | [optional]  |
| **adAccountId** | **string?** | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **campaignId** | **string?** | Platform campaign ID (filter ads within a campaign) | [optional]  |
| **platformAdId** | **string?** | Meta ad ID. Returns the ad with this platform-side ad ID. | [optional]  |
| **effectiveObjectStoryId** | **string?** | Facebook &#x60;{pageId}_{postId}&#x60; of the post the ad&#39;s engagement lives on (Meta &#x60;effective_object_story_id&#x60;). Use to map a Business-Manager-visible post back to the Zernio ad. | [optional]  |
| **effectiveInstagramMediaId** | **string?** | Instagram media ID of the boosted post (Meta &#x60;effective_instagram_media_id&#x60;). Use to map a Business-Manager-visible IG post back to the Zernio ad. | [optional]  |
| **fromDate** | **DateOnly?** | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |

### Return type

[**ListAds200Response**](ListAds200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated ads |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadsbusinesscenters"></a>
# **ListAdsBusinessCenters**
> ListAdsBusinessCenters200Response ListAdsBusinessCenters (string accountId)

List TikTok Business Centers

Returns the TikTok Business Centers (BCs) the connected `tiktokads` account can read. Each BC reports its advertiser count so callers can build agency-style pickers without re-walking `/v1/ads/accounts` per BC.  TikTok-only. Solo advertisers (non-agency tokens) return an empty array. 

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
    public class ListAdsBusinessCentersExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | ID of the `tiktokads` (or parent `tiktok` posting) SocialAccount

            try
            {
                // List TikTok Business Centers
                ListAdsBusinessCenters200Response result = apiInstance.ListAdsBusinessCenters(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.ListAdsBusinessCenters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdsBusinessCentersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List TikTok Business Centers
    ApiResponse<ListAdsBusinessCenters200Response> response = apiInstance.ListAdsBusinessCentersWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.ListAdsBusinessCentersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | ID of the &#x60;tiktokads&#x60; (or parent &#x60;tiktok&#x60; posting) SocialAccount |  |

### Return type

[**ListAdsBusinessCenters200Response**](ListAdsBusinessCenters200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Business centers |  -  |
| **401** | Unauthorized |  -  |
| **404** | TikTok account not found |  -  |
| **422** | TikTok Ads not connected |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconversionassociations"></a>
# **ListConversionAssociations**
> ListConversionAssociations200Response ListConversionAssociations (string accountId, string destinationId, string adAccountId)

List campaigns associated with a conversion destination

LinkedIn-only today. Returns the campaigns currently associated with this conversion rule. Note that auto-association on rule creation runs once at create time; campaigns created after the rule still need explicit association. 

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
    public class ListConversionAssociationsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 

            try
            {
                // List campaigns associated with a conversion destination
                ListConversionAssociations200Response result = apiInstance.ListConversionAssociations(accountId, destinationId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.ListConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaigns associated with a conversion destination
    ApiResponse<ListConversionAssociations200Response> response = apiInstance.ListConversionAssociationsWithHttpInfo(accountId, destinationId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.ListConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |

### Return type

[**ListConversionAssociations200Response**](ListConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Associations listed |  -  |
| **400** | Validation error. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | Account or destination not found. |  -  |
| **405** | Platform does not support associations. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listconversiondestinations"></a>
# **ListConversionDestinations**
> ListConversionDestinations200Response ListConversionDestinations (string accountId)

List destinations for the Conversions API

Returns the list of pixels (Meta), conversion actions (Google), or conversion rules (LinkedIn) accessible to the connected ads account. Use the returned `id` as `destinationId` when posting to `POST /v1/ads/conversions`.  For Google and LinkedIn, each destination's `type` reflects the conversion type (PURCHASE, LEAD, SIGN_UP, etc.) — the event type is locked to the destination. For Meta, `type` is absent: pixels accept any event name per request.  For LinkedIn, destinations are returned across every sponsored ad account the connected token can access; the `adAccountId` field on each destination identifies the parent ad account and is required for subsequent CRUD calls (update, delete, associations, metrics). 

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
    public class ListConversionDestinationsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | SocialAccount ID (metaads, googleads, or linkedinads).

            try
            {
                // List destinations for the Conversions API
                ListConversionDestinations200Response result = apiInstance.ListConversionDestinations(accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.ListConversionDestinations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListConversionDestinationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List destinations for the Conversions API
    ApiResponse<ListConversionDestinations200Response> response = apiInstance.ListConversionDestinationsWithHttpInfo(accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.ListConversionDestinationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | SocialAccount ID (metaads, googleads, or linkedinads). |  |

### Return type

[**ListConversionDestinations200Response**](ListConversionDestinations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destinations listed |  -  |
| **400** | Account&#39;s platform is not supported by the Conversions API. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), OR (for LinkedIn) the connected account lacks the &#x60;rw_conversions&#x60; scope and must be reconnected.  |  -  |
| **404** | Account not found or not accessible. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeconversionassociations"></a>
# **RemoveConversionAssociations**
> RemoveConversionAssociations200Response RemoveConversionAssociations (string accountId, string destinationId, string adAccountId, string campaignIds)

Remove campaign↔conversion associations

Remove one or more campaign associations from this conversion rule. Pass `adAccountId` and `campaignIds` as query parameters (`campaignIds` is comma-separated). The route also accepts a JSON body with the same fields for clients that prefer DELETE-with-body, but the documented surface is query-only because some SDK code generators (e.g. Python) collapse query + body parameters with the same name into a single kwarg. 

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
    public class RemoveConversionAssociationsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string | 
            var campaignIds = "campaignIds_example";  // string | Comma-separated list of campaign IDs.

            try
            {
                // Remove campaign↔conversion associations
                RemoveConversionAssociations200Response result = apiInstance.RemoveConversionAssociations(accountId, destinationId, adAccountId, campaignIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.RemoveConversionAssociations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveConversionAssociationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove campaign↔conversion associations
    ApiResponse<RemoveConversionAssociations200Response> response = apiInstance.RemoveConversionAssociationsWithHttpInfo(accountId, destinationId, adAccountId, campaignIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.RemoveConversionAssociationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **adAccountId** | **string** |  |  |
| **campaignIds** | **string** | Comma-separated list of campaign IDs. |  |

### Return type

[**RemoveConversionAssociations200Response**](RemoveConversionAssociations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-campaign batch result. Status is 200 even when some rows failed — inspect &#x60;failed[]&#x60; for details.  |  -  |
| **400** | Validation error: missing &#x60;adAccountId&#x60; or &#x60;campaignIds&#x60;, or campaignIds exceeds 100 entries per request.  |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | Account or destination not found. |  -  |
| **405** | Platform does not support associations. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="searchadinterests"></a>
# **SearchAdInterests**
> SearchAdInterests200Response SearchAdInterests (string q, string accountId)

Search targeting interests

Search for interest-based targeting options available on the platform.

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
    public class SearchAdInterestsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query
            var accountId = "accountId_example";  // string | Social account ID

            try
            {
                // Search targeting interests
                SearchAdInterests200Response result = apiInstance.SearchAdInterests(q, accountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.SearchAdInterests: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchAdInterestsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search targeting interests
    ApiResponse<SearchAdInterests200Response> response = apiInstance.SearchAdInterestsWithHttpInfo(q, accountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.SearchAdInterestsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query |  |
| **accountId** | **string** | Social account ID |  |

### Return type

[**SearchAdInterests200Response**](SearchAdInterests200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Matching interests |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="searchadtargetinglocations"></a>
# **SearchAdTargetingLocations**
> SearchAdTargetingLocations200Response SearchAdTargetingLocations (string accountId, string q, string? type = null, string? countryCode = null, int? limit = null)

Search geo targeting locations (Meta)

Resolve a human-readable location name into Meta's opaque `key` used in `targeting.cities[]` / `targeting.regions[]` on `POST /v1/ads/create` (and the same fields under `targeting.geo_locations` on `POST /v1/ads/boost`). Wraps Meta's `/search?type=adgeolocation` endpoint.  Meta-only for now. Other platforms have their own location id systems and are not exposed here.  Per Meta's docs, `q` must contain only the locality name (e.g. `\"Amsterdam\"`, not `\"Amsterdam, NL\"`). Use `countryCode` to disambiguate when the same name exists in multiple countries. 

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
    public class SearchAdTargetingLocationsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Social account ID (must be a connected Facebook or Instagram account).
            var q = "q_example";  // string | Location name. Locality only — no region/country suffix.
            var type = "country";  // string? | Type of location to search. Defaults to city. (optional)  (default to city)
            var countryCode = "countryCode_example";  // string? | ISO 3166-1 alpha-2 country code (e.g. NL) to scope the search. (optional) 
            var limit = 25;  // int? | Maximum results to return. (optional)  (default to 25)

            try
            {
                // Search geo targeting locations (Meta)
                SearchAdTargetingLocations200Response result = apiInstance.SearchAdTargetingLocations(accountId, q, type, countryCode, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.SearchAdTargetingLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchAdTargetingLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search geo targeting locations (Meta)
    ApiResponse<SearchAdTargetingLocations200Response> response = apiInstance.SearchAdTargetingLocationsWithHttpInfo(accountId, q, type, countryCode, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.SearchAdTargetingLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Social account ID (must be a connected Facebook or Instagram account). |  |
| **q** | **string** | Location name. Locality only — no region/country suffix. |  |
| **type** | **string?** | Type of location to search. Defaults to city. | [optional] [default to city] |
| **countryCode** | **string?** | ISO 3166-1 alpha-2 country code (e.g. NL) to scope the search. | [optional]  |
| **limit** | **int?** | Maximum results to return. | [optional] [default to 25] |

### Return type

[**SearchAdTargetingLocations200Response**](SearchAdTargetingLocations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Matching locations |  -  |
| **400** | Missing or invalid query parameters |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | Account not found, or platform does not support targeting search (Meta only) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendconversions"></a>
# **SendConversions**
> SendConversions200Response SendConversions (SendConversionsRequest sendConversionsRequest)

Send conversion events to an ad platform

Relay one or more conversion events to the target ad platform's native Conversions API. Platform is inferred from the provided `accountId`. Requires the Ads add-on.  Supported platforms:  - Meta (`metaads`) via Graph API - Google Ads (`googleads`) via Data Manager API `ingestEvents` - LinkedIn (`linkedinads`) via `/rest/conversionEvents`  `destinationId` semantics differ per platform:  - Meta: pixel (dataset) ID, e.g. `123456789012345` - Google: conversion action resource name, e.g. `customers/1234567890/conversionActions/987654321` - LinkedIn: conversion rule ID or URN, e.g. `104012` or `urn:lla:llaPartnerConversion:104012`  Callers can list valid destinations via `GET /v1/accounts/{accountId}/conversion-destinations`.  All PII (email, phone, names, external IDs) is hashed with SHA-256 server-side per each platform's normalization spec, including Google's Gmail-specific dot/plus-suffix stripping. Send plaintext. LinkedIn `externalIds` are passed through as plaintext per LinkedIn's spec; only emails and phones are hashed.  For LinkedIn, the connected account must have been authorized after the Conversions API rollout (i.e. the OAuth grant must include `rw_conversions`). Older accounts must reconnect.  Batching is handled automatically. Meta caps at 1000 events per request and rejects the entire batch if any event is malformed. Google caps at 2000. LinkedIn caps at 5000 and is also all-or-nothing per chunk.  Dedup: pass a stable `eventId` on every event. Meta and LinkedIn use it to dedupe against browser-side pixel/Insight Tag events; Google maps it to `transactionId`.  Per-platform `eventName` semantics:  - Meta: free-form. Standard names (Purchase, Lead, ...) match Meta's built-in events; custom strings are accepted. - Google: ignored. The conversion action's category determines the event type. Send the standard name closest to your action for documentation, but the platform will not branch on it. - LinkedIn: ignored. The conversion rule's `type` (LEAD, PURCHASE, etc.) is locked to the destination at rule-creation time. Send the standard name for documentation; LinkedIn does not branch on it. 

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
    public class SendConversionsExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var sendConversionsRequest = new SendConversionsRequest(); // SendConversionsRequest | 

            try
            {
                // Send conversion events to an ad platform
                SendConversions200Response result = apiInstance.SendConversions(sendConversionsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.SendConversions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendConversionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send conversion events to an ad platform
    ApiResponse<SendConversions200Response> response = apiInstance.SendConversionsWithHttpInfo(sendConversionsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.SendConversionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendConversionsRequest** | [**SendConversionsRequest**](SendConversionsRequest.md) |  |  |

### Return type

[**SendConversions200Response**](SendConversions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Events processed. Inspect &#x60;eventsFailed&#x60; and &#x60;failures[]&#x60; to detect partial failure. For Meta, a batch is all-or-nothing (either every event in a chunk succeeds, or every event in the chunk is listed in failures). For Google, the API returns success/failure at the request level only.  |  -  |
| **400** | Invalid body (missing accountId/destinationId/events, malformed event shape). |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans), OR (for LinkedIn) the connected account lacks the &#x60;rw_conversions&#x60; scope and must be reconnected.  |  -  |
| **404** | Account not found or not accessible. |  -  |
| **429** | LinkedIn token-level rate limit hit (600 requests/min, 300k/day per token). Retry with backoff. Meta and Google have their own rate-limit semantics surfaced via platform-specific 4xx responses.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendwhatsappconversion"></a>
# **SendWhatsAppConversion**
> SendWhatsAppConversion200Response SendWhatsAppConversion (SendWhatsAppConversionRequest sendWhatsAppConversionRequest)

Send WhatsApp conversion event

Forward a WhatsApp Business Messaging conversion event (`LeadSubmitted`, `Purchase`, `AddToCart`, `InitiateCheckout`, `ViewContent`) to Meta's Conversions API with `action_source = business_messaging` and `messaging_channel = whatsapp`. The endpoint looks up the originating CTWA click ID (`ctwa_clid`) captured on the first inbound message of the conversation and replays it on every event so Meta can attribute the conversion back to the Click-to-WhatsApp ad that drove the chat.  Configuration prerequisites on the WhatsApp account metadata:   - `metaCapiDatasetId`: the Meta Pixel/Dataset ID linked to the WABA.   - `connectedFacebookPageId`: the Facebook Page paired with the     WhatsApp Business number.  Identify the conversation by either `conversationId` (preferred) or `phoneE164` (digits only, no `+`). At least one is required. If the conversation has no captured `ctwa_clid`, the request returns 422 because there is nothing to attribute.  Token and dataset coupling: the WhatsApp account's accessToken must have access to the configured `metaCapiDatasetId`. By default a WABA's system-user token is scoped to the WABA's own Business Manager and cannot post to a pixel owned by a different Business; Meta returns code 100 in that case. Either share the dataset with the WhatsApp app's Business in BM, or use a dataset already in the same Business as the WABA. 

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
    public class SendWhatsAppConversionExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var sendWhatsAppConversionRequest = new SendWhatsAppConversionRequest(); // SendWhatsAppConversionRequest | 

            try
            {
                // Send WhatsApp conversion event
                SendWhatsAppConversion200Response result = apiInstance.SendWhatsAppConversion(sendWhatsAppConversionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.SendWhatsAppConversion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendWhatsAppConversionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send WhatsApp conversion event
    ApiResponse<SendWhatsAppConversion200Response> response = apiInstance.SendWhatsAppConversionWithHttpInfo(sendWhatsAppConversionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.SendWhatsAppConversionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sendWhatsAppConversionRequest** | [**SendWhatsAppConversionRequest**](SendWhatsAppConversionRequest.md) |  |  |

### Return type

[**SendWhatsAppConversion200Response**](SendWhatsAppConversion200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Event submitted to Meta. Inspect &#x60;eventsFailed&#x60; and &#x60;failures[]&#x60; to detect partial failures. A 200 does not mean Meta accepted the event; the status reflects \&quot;request reached Meta\&quot; only.  |  -  |
| **400** | Invalid body. |  -  |
| **401** | Unauthorized |  -  |
| **404** | Conversation not found. |  -  |
| **422** | Configuration missing (no &#x60;metaCapiDatasetId&#x60; / &#x60;connectedFacebookPageId&#x60; on the account) OR the resolved conversation has no captured &#x60;ctwa_clid&#x60;.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatead"></a>
# **UpdateAd**
> UpdateAd200Response UpdateAd (string adId, UpdateAdRequest updateAdRequest)

Update ad

Patch one or more fields on an ad. Status, budget, targeting, and creative changes are propagated to the platform.  Per-platform support: - **Meta** (Facebook + Instagram): all fields supported. - **TikTok**: status, budget, targeting (via `/v2/adgroup/update/`), and creative   (via `/v2/ad/update/` patch-style — `headline` is ignored, `body` becomes `ad_text`). - **Pinterest / X / LinkedIn / Google**: status + budget only. Sending `targeting`   or `creative` returns 501 with code `unsupported_platform_operation`. 

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
    public class UpdateAdExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 
            var updateAdRequest = new UpdateAdRequest(); // UpdateAdRequest | 

            try
            {
                // Update ad
                UpdateAd200Response result = apiInstance.UpdateAd(adId, updateAdRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.UpdateAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update ad
    ApiResponse<UpdateAd200Response> response = apiInstance.UpdateAdWithHttpInfo(adId, updateAdRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.UpdateAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** |  |  |
| **updateAdRequest** | [**UpdateAdRequest**](UpdateAdRequest.md) |  |  |

### Return type

[**UpdateAd200Response**](UpdateAd200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad updated |  -  |
| **400** | Invalid status transition or budget below minimum |  -  |
| **401** | Unauthorized |  -  |
| **404** | Resource not found |  -  |
| **501** | targeting or creative not supported on the platform (Meta + TikTok only) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateconversiondestination"></a>
# **UpdateConversionDestination**
> CreateConversionDestination201Response UpdateConversionDestination (string accountId, string destinationId, UpdateConversionDestinationRequest updateConversionDestinationRequest)

Update a conversion destination

Partial-update a conversion rule. LinkedIn-only today. Whitelisted fields: `name`, `enabled`, attribution windows, `valueType`, `value`, `attributionType`. The rule's `type` and parent ad account are intentionally not exposed for update — recreate the rule if those need to change. 

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
    public class UpdateConversionDestinationExample
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
            var apiInstance = new AdsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | 
            var destinationId = "destinationId_example";  // string | 
            var updateConversionDestinationRequest = new UpdateConversionDestinationRequest(); // UpdateConversionDestinationRequest | 

            try
            {
                // Update a conversion destination
                CreateConversionDestination201Response result = apiInstance.UpdateConversionDestination(accountId, destinationId, updateConversionDestinationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdsApi.UpdateConversionDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateConversionDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a conversion destination
    ApiResponse<CreateConversionDestination201Response> response = apiInstance.UpdateConversionDestinationWithHttpInfo(accountId, destinationId, updateConversionDestinationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdsApi.UpdateConversionDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** |  |  |
| **destinationId** | **string** |  |  |
| **updateConversionDestinationRequest** | [**UpdateConversionDestinationRequest**](UpdateConversionDestinationRequest.md) |  |  |

### Return type

[**CreateConversionDestination201Response**](CreateConversionDestination201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Destination updated (re-fetched canonical state) |  -  |
| **400** | Invalid body or LinkedIn validation failure. |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads add-on or LinkedIn reconnect required. |  -  |
| **404** | Account or destination not found. |  -  |
| **405** | Platform does not support updating destinations. |  -  |
| **429** | LinkedIn rate limit hit. Retry with backoff. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

