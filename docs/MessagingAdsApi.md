# Zernio.Api.MessagingAdsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCallAd**](MessagingAdsApi.md#createcallad) | **POST** /v1/ads/call | Create Click-to-Call ad |
| [**CreateCtwaAd**](MessagingAdsApi.md#createctwaad) | **POST** /v1/ads/ctwa | Create Click-to-WhatsApp ad (deprecated) |
| [**CreateMessagingAd**](MessagingAdsApi.md#createmessagingad) | **POST** /v1/ads/messaging | Create click-to-message ad (WhatsApp / Messenger / Instagram Direct) |

<a id="createcallad"></a>
# **CreateCallAd**
> void CreateCallAd (CreateCallAdRequest createCallAdRequest)

Create Click-to-Call ad

Same shape and flow as POST /v1/ads/ctwa, but the CTA is CALL_NOW dialing `phoneNumber` via a tel: link. The ad set is destination_type PHONE_CALL optimizing QUALITY_CALL and the campaign objective defaults to OUTCOME_LEADS. Supports the same single-creative and multi-creative shapes as CTWA.

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
    public class CreateCallAdExample
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
            var apiInstance = new MessagingAdsApi(httpClient, config, httpClientHandler);
            var createCallAdRequest = new CreateCallAdRequest(); // CreateCallAdRequest | 

            try
            {
                // Create Click-to-Call ad
                apiInstance.CreateCallAd(createCallAdRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagingAdsApi.CreateCallAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCallAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Click-to-Call ad
    apiInstance.CreateCallAdWithHttpInfo(createCallAdRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagingAdsApi.CreateCallAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCallAdRequest** | [**CreateCallAdRequest**](CreateCallAdRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Ad(s) created and submitted for review |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |
| **422** | No Facebook Page resolved for the account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createctwaad"></a>
# **CreateCtwaAd**
> CreateCtwaAd201Response CreateCtwaAd (CtwaAdRequestBody ctwaAdRequestBody)

Create Click-to-WhatsApp ad (deprecated)

Deprecated: use POST /v1/ads/messaging with `destination: whatsapp`. This endpoint stays available for back-compat; no removal planned.  Creates one or more Click-to-WhatsApp (CTWA) ads on Meta under a single campaign and ad set. When tapped, each ad opens a WhatsApp conversation with the business attached to the supplied Facebook Page. The full hierarchy (campaign, ad set, creative(s), ad(s)) is created and activated in one call. The CTA is locked to WHATSAPP_MESSAGE and the destination is hard-coded to api.whatsapp.com/send; Meta resolves the actual WhatsApp number from the Page-to-WA pairing configured in Page settings or Business Manager.  Supports two mutually-exclusive shapes:  - **Single-creative**: supply top-level `headline`, `body`, and one of `imageUrl` / `video`. Creates 1 campaign + 1 ad set + 1 ad.  - **Multi-creative**: supply a `creatives[]` array with N entries (each carrying its own headline, body, and image/video). Creates 1 campaign + 1 ad set + N ads sharing budget and targeting so Meta A/Bs the creatives inside a single auction instead of fragmenting budget across N parallel campaigns. Recommended when launching multiple creative variants for the same campaign.  Prerequisites enforced by Meta (surfaced as platform_error on failure): the Facebook Page must be paired with a verified WhatsApp Business number, the WhatsApp Business Account must be business-verified, and the Meta access token must carry ads_management.

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
            var apiInstance = new MessagingAdsApi(httpClient, config, httpClientHandler);
            var ctwaAdRequestBody = new CtwaAdRequestBody(); // CtwaAdRequestBody | 

            try
            {
                // Create Click-to-WhatsApp ad (deprecated)
                CreateCtwaAd201Response result = apiInstance.CreateCtwaAd(ctwaAdRequestBody);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagingAdsApi.CreateCtwaAd: " + e.Message);
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
    // Create Click-to-WhatsApp ad (deprecated)
    ApiResponse<CreateCtwaAd201Response> response = apiInstance.CreateCtwaAdWithHttpInfo(ctwaAdRequestBody);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagingAdsApi.CreateCtwaAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ctwaAdRequestBody** | [**CtwaAdRequestBody**](CtwaAdRequestBody.md) |  |  |

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

<a id="createmessagingad"></a>
# **CreateMessagingAd**
> void CreateMessagingAd (CreateMessagingAdRequest createMessagingAdRequest)

Create click-to-message ad (WhatsApp / Messenger / Instagram Direct)

Creates a click-to-message ad; `destination` selects where the tapped ad opens a conversation: WhatsApp, the Page's Messenger inbox or the linked Instagram account's Direct inbox. The ad set is created with the matching destination_type and CONVERSATIONS optimization; the campaign objective defaults to OUTCOME_ENGAGEMENT. Supports single-creative and multi-creative shapes. Supersedes POST /v1/ads/ctwa (deprecated, equivalent to `destination: whatsapp`).

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
    public class CreateMessagingAdExample
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
            var apiInstance = new MessagingAdsApi(httpClient, config, httpClientHandler);
            var createMessagingAdRequest = new CreateMessagingAdRequest(); // CreateMessagingAdRequest | 

            try
            {
                // Create click-to-message ad (WhatsApp / Messenger / Instagram Direct)
                apiInstance.CreateMessagingAd(createMessagingAdRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MessagingAdsApi.CreateMessagingAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateMessagingAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create click-to-message ad (WhatsApp / Messenger / Instagram Direct)
    apiInstance.CreateMessagingAdWithHttpInfo(createMessagingAdRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MessagingAdsApi.CreateMessagingAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createMessagingAdRequest** | [**CreateMessagingAdRequest**](CreateMessagingAdRequest.md) |  |  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Ad(s) created and submitted for review |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Account not found |  -  |
| **422** | No Facebook Page resolved for the account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

