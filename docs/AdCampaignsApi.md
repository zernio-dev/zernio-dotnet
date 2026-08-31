# Zernio.Api.AdCampaignsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AttachCampaignAssets**](AdCampaignsApi.md#attachcampaignassets) | **POST** /v1/ads/campaigns/{campaignId}/assets | Attach extension assets to a Google Search campaign |
| [**BoostPost**](AdCampaignsApi.md#boostpost) | **POST** /v1/ads/boost | Boost post as ad |
| [**BulkUpdateAdCampaignStatus**](AdCampaignsApi.md#bulkupdateadcampaignstatus) | **POST** /v1/ads/campaigns/bulk-status | Pause or resume many campaigns |
| [**CreateAdCampaign**](AdCampaignsApi.md#createadcampaign) | **POST** /v1/ads/campaigns | Create a standalone campaign |
| [**CreateStandaloneAd**](AdCampaignsApi.md#createstandalonead) | **POST** /v1/ads/create | Create standalone ad |
| [**DeleteAd**](AdCampaignsApi.md#deletead) | **DELETE** /v1/ads/{adId} | Cancel an ad |
| [**DeleteAdCampaign**](AdCampaignsApi.md#deleteadcampaign) | **DELETE** /v1/ads/campaigns/{campaignId} | Delete a campaign |
| [**DeleteAdSet**](AdCampaignsApi.md#deleteadset) | **DELETE** /v1/ads/ad-sets/{adSetId} | Delete an ad set |
| [**DuplicateAd**](AdCampaignsApi.md#duplicatead) | **POST** /v1/ads/{adId}/duplicate | Duplicate an ad |
| [**DuplicateAdCampaign**](AdCampaignsApi.md#duplicateadcampaign) | **POST** /v1/ads/campaigns/{campaignId}/duplicate | Duplicate a campaign |
| [**DuplicateAdSet**](AdCampaignsApi.md#duplicateadset) | **POST** /v1/ads/ad-sets/{adSetId}/duplicate | Duplicate an ad set |
| [**GetAd**](AdCampaignsApi.md#getad) | **GET** /v1/ads/{adId} | Get ad details |
| [**GetAdSetDetails**](AdCampaignsApi.md#getadsetdetails) | **GET** /v1/ads/ad-sets/{adSetId} | Live ad-set details incl. learning phase |
| [**GetAdTree**](AdCampaignsApi.md#getadtree) | **GET** /v1/ads/tree | Get campaign tree |
| [**GetAdsTimeline**](AdCampaignsApi.md#getadstimeline) | **GET** /v1/ads/timeline | Get daily account metrics |
| [**ListAdCampaigns**](AdCampaignsApi.md#listadcampaigns) | **GET** /v1/ads/campaigns | List campaigns |
| [**ListAdKeywords**](AdCampaignsApi.md#listadkeywords) | **GET** /v1/ads/keywords | List Search keywords |
| [**ListAds**](AdCampaignsApi.md#listads) | **GET** /v1/ads | List ads |
| [**UpdateAd**](AdCampaignsApi.md#updatead) | **PUT** /v1/ads/{adId} | Update ad |
| [**UpdateAdCampaign**](AdCampaignsApi.md#updateadcampaign) | **PUT** /v1/ads/campaigns/{campaignId} | Update a campaign |
| [**UpdateAdCampaignStatus**](AdCampaignsApi.md#updateadcampaignstatus) | **PUT** /v1/ads/campaigns/{campaignId}/status | Pause or resume a campaign |
| [**UpdateAdSet**](AdCampaignsApi.md#updateadset) | **PUT** /v1/ads/ad-sets/{adSetId} | Update an ad set |
| [**UpdateAdSetStatus**](AdCampaignsApi.md#updateadsetstatus) | **PUT** /v1/ads/ad-sets/{adSetId}/status | Pause or resume a single ad set |
| [**UpdateAdStatus**](AdCampaignsApi.md#updateadstatus) | **PUT** /v1/ads/{adId}/status | Pause or resume a single ad |

<a id="attachcampaignassets"></a>
# **AttachCampaignAssets**
> AttachCampaignAssets201Response AttachCampaignAssets (string campaignId, AttachCampaignAssetsRequest attachCampaignAssetsRequest)

Attach extension assets to a Google Search campaign

Attach sitelinks, callouts and/or structured snippets to an already-existing Google Search campaign — the same builders POST /v1/ads/create uses, but without rebuilding the hierarchy. At least one of sitelinks, callouts or structuredSnippets is required.  Google-only. Other platforms have no equivalent extension surface and return 501.  Approval status is Google-async; poll `asset.policy_summary` after review. Assets stay in the account library even if the campaign is later deleted.

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
    public class AttachCampaignAssetsExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Numeric Google platform campaign id.
            var attachCampaignAssetsRequest = new AttachCampaignAssetsRequest(); // AttachCampaignAssetsRequest | 

            try
            {
                // Attach extension assets to a Google Search campaign
                AttachCampaignAssets201Response result = apiInstance.AttachCampaignAssets(campaignId, attachCampaignAssetsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.AttachCampaignAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AttachCampaignAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Attach extension assets to a Google Search campaign
    ApiResponse<AttachCampaignAssets201Response> response = apiInstance.AttachCampaignAssetsWithHttpInfo(campaignId, attachCampaignAssetsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.AttachCampaignAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Numeric Google platform campaign id. |  |
| **attachCampaignAssetsRequest** | [**AttachCampaignAssetsRequest**](AttachCampaignAssetsRequest.md) |  |  |

### Return type

[**AttachCampaignAssets201Response**](AttachCampaignAssets201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Assets attached |  -  |
| **400** | Invalid input, Google rejected the assets, an unknown customerId (not one of this connection&#39;s Google Ads accounts), or a required customerId missing when the connection has multiple Google Ads accounts |  -  |
| **401** | Unauthorized |  -  |
| **422** | No Google Ads customer accounts on this connection. Reconnect Google Ads. |  -  |
| **501** | Only supported on Google Ads |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="boostpost"></a>
# **BoostPost**
> UpdateAd200Response BoostPost (BoostPostRequest boostPostRequest, string? idempotencyKey = null)

Boost post as ad

Creates a paid ad from an existing published post, keeping the post's engagement. By default it provisions the whole hierarchy (campaign, ad set, ad).  **Attach shape (Meta).** Send `adSetId` to put the ad under an EXISTING ad set instead, so that ad set keeps its learning phase. It then owns `budget`, `schedule` and `targeting`, and sending any of those alongside `adSetId` is a 400 rather than a silent drop. `budget` is required only without `adSetId`.  `instagramAccountId`, `destinationType` and `adSetId` are Meta-only and return 400 on other platforms.  **Retries.** Boosts are NOT idempotent and can take minutes when Meta requires re-hosting an Instagram video, so do not retry on client timeout. Send an Idempotency-Key header to make retries safe: same key and body replays the original 201, and distinct keys always create distinct ads. Without the header, an identical request is treated as a retry: while one is in flight it returns 409, and within 10 minutes of a completed boost it returns the already-created ad instead of creating another. To intentionally duplicate an ad, send distinct Idempotency-Keys (or vary the body, e.g. the name). 

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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var boostPostRequest = new BoostPostRequest(); // BoostPostRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Boost post as ad
                UpdateAd200Response result = apiInstance.BoostPost(boostPostRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.BoostPost: " + e.Message);
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
    ApiResponse<UpdateAd200Response> response = apiInstance.BoostPostWithHttpInfo(boostPostRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.BoostPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **boostPostRequest** | [**BoostPostRequest**](BoostPostRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

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
| **409** | An identical boost request is already in progress (with or without an Idempotency-Key). Wait for it to finish instead of retrying.  |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads), missing linked account, or — for TikTok — the connected TikTok user is not authorized as an Identity on the target advertiser. Returned with code &#x60;ads_connection_required&#x60;; the message includes the actionable \&quot;TikTok Ads Manager → Assets → Identity\&quot; remediation step. Also returned as &#x60;idempotency_key_reused&#x60; when an Idempotency-Key is reused with a different request body.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bulkupdateadcampaignstatus"></a>
# **BulkUpdateAdCampaignStatus**
> BulkUpdateAdCampaignStatus200Response BulkUpdateAdCampaignStatus (BulkUpdateAdCampaignStatusRequest bulkUpdateAdCampaignStatusRequest)

Pause or resume many campaigns

Process up to 50 campaigns in one call. Each campaign is updated concurrently and the response contains a per-campaign result so a single bad row does not fail the whole batch. 

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
    public class BulkUpdateAdCampaignStatusExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var bulkUpdateAdCampaignStatusRequest = new BulkUpdateAdCampaignStatusRequest(); // BulkUpdateAdCampaignStatusRequest | 

            try
            {
                // Pause or resume many campaigns
                BulkUpdateAdCampaignStatus200Response result = apiInstance.BulkUpdateAdCampaignStatus(bulkUpdateAdCampaignStatusRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.BulkUpdateAdCampaignStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BulkUpdateAdCampaignStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause or resume many campaigns
    ApiResponse<BulkUpdateAdCampaignStatus200Response> response = apiInstance.BulkUpdateAdCampaignStatusWithHttpInfo(bulkUpdateAdCampaignStatusRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.BulkUpdateAdCampaignStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **bulkUpdateAdCampaignStatusRequest** | [**BulkUpdateAdCampaignStatusRequest**](BulkUpdateAdCampaignStatusRequest.md) |  |  |

### Return type

[**BulkUpdateAdCampaignStatus200Response**](BulkUpdateAdCampaignStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-campaign results |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcampaign"></a>
# **CreateAdCampaign**
> CreateAdCampaign201Response CreateAdCampaign (CreateAdCampaignRequest createAdCampaignRequest, string? idempotencyKey = null)

Create a standalone campaign

Creates a campaign WITHOUT its first ad set / ad (the ODAX shell only). Ad sets join it later via `existingCampaignId` on the create endpoints. A budget here is campaign-level (CBO) by definition; omit it for ABO (each ad set carries its own budget). Created `PAUSED` unless `status: ACTIVE`. The campaign materializes in `/v1/ads/tree` via the next sync discovery pass.  **Idempotency:** send an `Idempotency-Key` header to make retries safe.

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
    public class CreateAdCampaignExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var createAdCampaignRequest = new CreateAdCampaignRequest(); // CreateAdCampaignRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. (optional) 

            try
            {
                // Create a standalone campaign
                CreateAdCampaign201Response result = apiInstance.CreateAdCampaign(createAdCampaignRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.CreateAdCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a standalone campaign
    ApiResponse<CreateAdCampaign201Response> response = apiInstance.CreateAdCampaignWithHttpInfo(createAdCampaignRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.CreateAdCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdCampaignRequest** | [**CreateAdCampaignRequest**](CreateAdCampaignRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. | [optional]  |

### Return type

[**CreateAdCampaign201Response**](CreateAdCampaign201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Campaign created |  -  |
| **400** | Invalid input, or Meta rejected the create |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createstandalonead"></a>
# **CreateStandaloneAd**
> CreateStandaloneAd200Response CreateStandaloneAd (CreateStandaloneAdRequest createStandaloneAdRequest, string? idempotencyKey = null)

Create standalone ad

Creates a paid ad with custom creative across Meta, Google Ads, Pinterest, TikTok, X/Twitter, LinkedIn, and OpenAI Ads (ChatGPT Ads). Supports three mutually-exclusive request shapes selected by the body, a legacy single-creative shape (all platforms, default), a Meta-only multi-creative shape via the creatives array (one ad set with N ads sharing budget and targeting), and an attach shape via adSetId that adds one new ad to an existing ad set, inheriting its budget, targeting, and schedule (Meta, TikTok, and LinkedIn; on LinkedIn adSetId is the existing Campaign id, and the budget, schedule, targeting and bidding fields must be omitted). Per-platform required fields, budget minimums, and video-ad rules are documented on each property below. LinkedIn creates a Single Image or Single Video Ad backed by a Direct Sponsored Content \"dark post\" authored by a Company Page (see `organizationId`); supported goals are engagement, traffic, awareness, and video_views (video ads use the `video` field; video_views requires a video), and traffic ads require `linkUrl`.  **Idempotency:** this endpoint is not idempotent at the platform level (a blind retry creates a second campaign/ad set/ad). Send an `Idempotency-Key` header to make retries safe: the first request with a given key creates the ad and we store the response; a retry with the same key replays that exact response (with `Idempotent-Replayed: true`) instead of creating duplicates. Reusing a key with a different body returns 422; a key whose first request is still in flight returns 409 (retry after a short backoff). Keys are scoped to your credential and expire after 24h.

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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var createStandaloneAdRequest = new CreateStandaloneAdRequest(); // CreateStandaloneAdRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. (optional) 

            try
            {
                // Create standalone ad
                CreateStandaloneAd200Response result = apiInstance.CreateStandaloneAd(createStandaloneAdRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.CreateStandaloneAd: " + e.Message);
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
    ApiResponse<CreateStandaloneAd200Response> response = apiInstance.CreateStandaloneAdWithHttpInfo(createStandaloneAdRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.CreateStandaloneAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createStandaloneAdRequest** | [**CreateStandaloneAdRequest**](CreateStandaloneAdRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. | [optional]  |

### Return type

[**CreateStandaloneAd200Response**](CreateStandaloneAd200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | validateOnly dry-run passed — nothing was created |  -  |
| **201** | Ad(s) created |  -  |
| **400** | Missing required fields, invalid values, non-Meta platform used with creatives[] / adSetId, or a Meta validateOnly validation failure (verbatim) |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads) or missing linked account |  -  |
| **502** | The platform rejected the request, or failed to produce media the ad needs (e.g. Meta generated no poster for an uploaded video when no &#x60;video.thumbnailUrl&#x60; was supplied). Inspect &#x60;platformError&#x60; for the upstream payload. Failures we raise carry a &#x60;reason&#x60;; a payload forwarded verbatim from Meta may not. On the &#x60;creatives[]&#x60; shape a missing poster also carries &#x60;creativeIndex&#x60; and &#x60;videoUrl&#x60; to identify the entry. An upstream 4xx status is forwarded instead of 502.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletead"></a>
# **DeleteAd**
> DeleteAccountGroup200Response DeleteAd (string adId)

Cancel an ad

Cancels the ad on the platform and marks it as cancelled in the database. The ad is preserved for history. OpenAI Ads has no delete API; the ad is archived instead (a terminal state, the closest equivalent).

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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 

            try
            {
                // Cancel an ad
                DeleteAccountGroup200Response result = apiInstance.DeleteAd(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.DeleteAd: " + e.Message);
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
    Debug.Print("Exception when calling AdCampaignsApi.DeleteAdWithHttpInfo: " + e.Message);
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

<a id="deleteadcampaign"></a>
# **DeleteAdCampaign**
> DeleteAdCampaign200Response DeleteAdCampaign (string campaignId, DeleteAdCampaignRequest deleteAdCampaignRequest)

Delete a campaign

Deletes the whole campaign on the platform, cascading to its ad sets and ads. Locally, all Ad documents for this campaign are marked `status: cancelled`.  **Empty campaigns.** A campaign with zero ads has no local Ad documents to resolve, so it is invisible to `/v1/ads/tree` and this endpoint would 404. That state is produced by the two-step create flow (campaign, then ads via `existingCampaignId`) whenever Meta rejects the ad step. To delete such a shell, send `accountId` in the body: we skip the local lookup entirely and forward the delete to Meta. `accountId` is ignored when the campaign does have ads. 

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
    public class DeleteAdCampaignExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Platform campaign ID
            var deleteAdCampaignRequest = new DeleteAdCampaignRequest(); // DeleteAdCampaignRequest | 

            try
            {
                // Delete a campaign
                DeleteAdCampaign200Response result = apiInstance.DeleteAdCampaign(campaignId, deleteAdCampaignRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.DeleteAdCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete a campaign
    ApiResponse<DeleteAdCampaign200Response> response = apiInstance.DeleteAdCampaignWithHttpInfo(campaignId, deleteAdCampaignRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.DeleteAdCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Platform campaign ID |  |
| **deleteAdCampaignRequest** | [**DeleteAdCampaignRequest**](DeleteAdCampaignRequest.md) |  |  |

### Return type

[**DeleteAdCampaign200Response**](DeleteAdCampaign200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign deleted |  -  |
| **401** | Unauthorized |  -  |
| **404** | Campaign not found |  -  |
| **501** | Operation not supported on this platform |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deleteadset"></a>
# **DeleteAdSet**
> DeleteAdSet200Response DeleteAdSet (string adSetId)

Delete an ad set

Deletes the ad set on the platform, cascading to its ads only (never the campaign). Locally, every Ad document under the ad set is marked `status: cancelled`.  Delete is soft on platforms that have no hard delete: LinkedIn moves the campaign to `PENDING_DELETION`, Pinterest archives the ad group, and X soft-flags the line item. Google removes the ad group. All remain readable for reporting. 

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
    public class DeleteAdSetExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adSetId = "adSetId_example";  // string | Platform ad set ID

            try
            {
                // Delete an ad set
                DeleteAdSet200Response result = apiInstance.DeleteAdSet(adSetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.DeleteAdSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAdSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete an ad set
    ApiResponse<DeleteAdSet200Response> response = apiInstance.DeleteAdSetWithHttpInfo(adSetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.DeleteAdSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Platform ad set ID |  |

### Return type

[**DeleteAdSet200Response**](DeleteAdSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad set deleted |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad set not found |  -  |
| **501** | Operation not supported on this platform |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicatead"></a>
# **DuplicateAd**
> DuplicateAd200Response DuplicateAd (string adId, string? idempotencyKey = null, DuplicateAdRequest? duplicateAdRequest = null)

Duplicate an ad

Duplicates a single ad via Meta's native `POST /{ad-id}/copies`. The copy is created paused. `adSetId` retargets the copy into another ad set; omitted = the source's own ad set. Accepts the Zernio ad id or the platform ad id. Sync discovery is triggered automatically (`syncAfter: false` to skip).

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
    public class DuplicateAdExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Zernio ad ID or platform ad ID
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. (optional) 
            var duplicateAdRequest = new DuplicateAdRequest?(); // DuplicateAdRequest? |  (optional) 

            try
            {
                // Duplicate an ad
                DuplicateAd200Response result = apiInstance.DuplicateAd(adId, idempotencyKey, duplicateAdRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.DuplicateAd: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateAdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate an ad
    ApiResponse<DuplicateAd200Response> response = apiInstance.DuplicateAdWithHttpInfo(adId, idempotencyKey, duplicateAdRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.DuplicateAdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Zernio ad ID or platform ad ID |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. | [optional]  |
| **duplicateAdRequest** | [**DuplicateAdRequest?**](DuplicateAdRequest?.md) |  | [optional]  |

### Return type

[**DuplicateAd200Response**](DuplicateAd200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad duplicated |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad not found |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicateadcampaign"></a>
# **DuplicateAdCampaign**
> DuplicateAdCampaign200Response DuplicateAdCampaign (string campaignId, DuplicateAdCampaignRequest duplicateAdCampaignRequest, string? idempotencyKey = null)

Duplicate a campaign

Duplicates a campaign, including its ad sets, ads, creatives, and targeting by default (`deepCopy: true`). The copy is created paused so callers can review before launching.  Per-platform implementation: - **Meta** uses the native `POST /{campaign-id}/copies` endpoint. - **TikTok** has no native copy primitive; Zernio walks the source   graph (`/v2/campaign/get/`, `/v2/adgroup/get/`, `/v2/ad/get/`) and   recreates each entity via the corresponding `/create/` endpoints,   carrying over budget / targeting / bid_type / bid_price /   deep_bid_type / creative fields. Spark Ad linkage (`tiktok_item_id`)   is preserved. - **LinkedIn** has no native copy primitive; Zernio walks the source   CampaignGroup → Campaigns → Creatives and recreates each entity,   carrying over `type` / `costType` / `unitCost` /   `optimizationTargetType` / `creativeSelection` / `objectiveType` /   `format` / `dailyBudget` / `totalBudget` / `targetingCriteria` /   `runSchedule` and every Creative's `content` object verbatim.   `statusOption: INHERITED_FROM_SOURCE` is evaluated **per entity**:   any Group / Campaign / Creative whose source is `ACTIVE` gets its   clone activated too. Duplicating an ACTIVE campaign with   `INHERITED_FROM_SOURCE` starts a second front of spend the moment   the clone activates — the safe default is `PAUSED`.  The new hierarchy is asynchronous to materialize in our DB — we trigger sync discovery automatically. Set `syncAfter: false` to skip and poll `/v1/ads/tree` on your own cadence.  Other platforms return 501 Not Implemented. 

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
    public class DuplicateAdCampaignExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Source platform campaign ID
            var duplicateAdCampaignRequest = new DuplicateAdCampaignRequest(); // DuplicateAdCampaignRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. (optional) 

            try
            {
                // Duplicate a campaign
                DuplicateAdCampaign200Response result = apiInstance.DuplicateAdCampaign(campaignId, duplicateAdCampaignRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.DuplicateAdCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateAdCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate a campaign
    ApiResponse<DuplicateAdCampaign200Response> response = apiInstance.DuplicateAdCampaignWithHttpInfo(campaignId, duplicateAdCampaignRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.DuplicateAdCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Source platform campaign ID |  |
| **duplicateAdCampaignRequest** | [**DuplicateAdCampaignRequest**](DuplicateAdCampaignRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. | [optional]  |

### Return type

[**DuplicateAdCampaign200Response**](DuplicateAdCampaign200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign duplicated |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Source campaign not found |  -  |
| **501** | Operation not supported on this platform |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicateadset"></a>
# **DuplicateAdSet**
> DuplicateAdSet200Response DuplicateAdSet (string adSetId, DuplicateAdSetRequest duplicateAdSetRequest, string? idempotencyKey = null)

Duplicate an ad set

Duplicates an ad set, including its ads and creatives by default (`deepCopy: true`), via Meta's native `POST /{adset-id}/copies`. The copy is created paused so callers can review before launching. `campaignId` retargets the copy into another campaign; omitted = the source's own campaign. The new hierarchy materializes asynchronously — sync discovery is triggered automatically (`syncAfter: false` to skip).

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
    public class DuplicateAdSetExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adSetId = "adSetId_example";  // string | Source platform ad set ID
            var duplicateAdSetRequest = new DuplicateAdSetRequest(); // DuplicateAdSetRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. (optional) 

            try
            {
                // Duplicate an ad set
                DuplicateAdSet200Response result = apiInstance.DuplicateAdSet(adSetId, duplicateAdSetRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.DuplicateAdSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateAdSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate an ad set
    ApiResponse<DuplicateAdSet200Response> response = apiInstance.DuplicateAdSetWithHttpInfo(adSetId, duplicateAdSetRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.DuplicateAdSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Source platform ad set ID |  |
| **duplicateAdSetRequest** | [**DuplicateAdSetRequest**](DuplicateAdSetRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. | [optional]  |

### Return type

[**DuplicateAdSet200Response**](DuplicateAdSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad set duplicated |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Source ad set not found |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Zernio `_id` (hex), Meta `platformAdId` (numeric), or one of the creative's effective story/media IDs. See description for details. 

            try
            {
                // Get ad details
                GetAd200Response result = apiInstance.GetAd(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetAd: " + e.Message);
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
    Debug.Print("Exception when calling AdCampaignsApi.GetAdWithHttpInfo: " + e.Message);
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

<a id="getadsetdetails"></a>
# **GetAdSetDetails**
> GetAdSetDetails200Response GetAdSetDetails (string adSetId, string accountId, string? fields = null)

Live ad-set details incl. learning phase

Reads the ad set live from Meta, returned verbatim. The default projection includes `learning_stage_info` (learning-phase status: LEARNING / SUCCESS / FAIL / WAIVING — Meta omits its `status` key on paused ad sets), delivery settings, budgets, schedule and targeting. `fields` is a raw-passthrough override; unknown fields return Meta's 400 verbatim.

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
    public class GetAdSetDetailsExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adSetId = "adSetId_example";  // string | Meta ad set id (platformAdSetId).
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var fields = "fields_example";  // string? | Comma-separated Graph field override (supports nested {} projections). (optional) 

            try
            {
                // Live ad-set details incl. learning phase
                GetAdSetDetails200Response result = apiInstance.GetAdSetDetails(adSetId, accountId, fields);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetAdSetDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdSetDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Live ad-set details incl. learning phase
    ApiResponse<GetAdSetDetails200Response> response = apiInstance.GetAdSetDetailsWithHttpInfo(adSetId, accountId, fields);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetAdSetDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Meta ad set id (platformAdSetId). |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **fields** | **string?** | Comma-separated Graph field override (supports nested {} projections). | [optional]  |

### Return type

[**GetAdSetDetails200Response**](GetAdSetDetails200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The ad set as returned by Meta |  -  |
| **400** | Invalid input, or Meta rejected the query — message carries Meta&#39;s error |  -  |
| **401** | Unauthorized |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadtree"></a>
# **GetAdTree**
> AdTreeResponse GetAdTree (int? page = null, int? limit = null, string? source = null, string? platform = null, AdStatus? status = null, string? adAccountId = null, string? pageId = null, string? accountId = null, string? profileId = null, string? campaignId = null, DateOnly? fromDate = null, DateOnly? toDate = null, bool? hasDelivery = null, decimal? minSpend = null, string? sort = null, int? timeIncrement = null, string? dailyLevel = null)

Get campaign tree

Returns a nested Campaign > Ad Set > Ad hierarchy with rolled-up metrics at each level. Uses a two-stage aggregation: ads are grouped into ad sets, then ad sets into campaigns. Metrics are computed over an optional date range, then rolled up from ad level to ad set and campaign levels. Pagination is at the campaign level. Ads without a campaign or ad set ID are grouped into synthetic \"Ungrouped\" buckets. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max.  Pass `timeIncrement=1` to also get a daily breakdown: each node gains a `daily[]` array of per-day metrics (same fields as the aggregated `metrics`) in the same call. Use `dailyLevel` (`campaign` default, or `adset` / `ad`) to choose which levels carry the series. This replaces calling the tree once per day for per-campaign daily trends.  **Deleted objects stay in the tree.** Deleting an ad or a campaign is a soft delete: the Ad documents move to `status: cancelled` and are kept indefinitely, so their historical spend still counts toward the metrics of any date range they fall in. There is no pruning job and no retention window. Filter on `status` if your view should hide them, but do that after reading the totals, not before. 

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
    public class GetAdTreeExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var page = 1;  // int? | Page number (1-based) (optional)  (default to 1)
            var limit = 20;  // int? | Campaigns per page (optional)  (default to 20)
            var source = "zernio";  // string? | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager — matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default — use the `status` param for that. (optional)  (default to all)
            var platform = "facebook";  // string? |  (optional) 
            var status = new AdStatus?(); // AdStatus? | Filter by derived campaign status (post-aggregation) (optional) 
            var adAccountId = "adAccountId_example";  // string? | One or more platform ad account IDs to scope the tree to (agency profiles connect a whole Business Manager but a workspace usually cares about a subset). Comma-separate for multiple (`?adAccountId=act_1,act_2,act_3`); single value keeps its old shape. Max 50 accounts per request; the plural aliases `adAccountIds` and `platformAdAccountIds` are rejected with a 400 to stop them from silently returning the unfiltered fleet. (optional) 
            var pageId = "pageId_example";  // string? | Meta only: Facebook Page ID. Prunes the tree to ads whose creative is backed by this Page — campaigns and ad sets with no ad on the Page drop out, and rolled-up metrics cover only the Page's ads. Mirrors the same filter on /v1/ads and /v1/ads/campaigns. (optional) 
            var accountId = "accountId_example";  // string? | Social account ID (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var campaignId = "campaignId_example";  // string? | Restrict the tree to a single campaign by its platform campaign id (the id the platform assigns, e.g. Meta's numeric campaign id). Filters the campaign set itself, so it works regardless of account size and pagination — pass this when you already hold a campaign id instead of paging the tree to find it. Mirrors the `campaignId` filter on GET /v1/ads. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of the METRICS date range (YYYY-MM-DD). On its own it affects only the spend/impression numbers overlaid on each node, not which campaigns are returned — pass `hasDelivery` or `minSpend` to also filter the campaign set to this window. Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 
            var hasDelivery = true;  // bool? | Return only campaigns that delivered between `fromDate` and `toDate` — spend above zero, or impressions served at zero spend. Unlike `status`, which reads a campaign's CURRENT state, this filters on what happened inside the window, so a campaign that spent then and is paused today is still returned. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. (optional) 
            var minSpend = 8.14D;  // decimal? | Return only campaigns whose spend between `fromDate` and `toDate` reaches this amount. Expressed in each campaign's OWN currency (the `currency` field on the campaign node): spend is stored per ad account in its native currency and one response can span several. Implies `hasDelivery`; `minSpend=0` applies no filter. (optional) 
            var sort = "newest";  // string? | Campaign-level sort order. `newest` (default) / `oldest` order by the campaign's newest-ad createdAt. `spend_desc` / `spend_asc` order by aggregated spend in the requested date range; campaigns with no spend land at the end. (optional)  (default to newest)
            var timeIncrement = 1;  // int? | Set to `1` to also return a daily breakdown. Mirrors Meta Insights' `time_increment=1`: each node gains a `daily[]` array of per-day metrics (same fields as the aggregated `metrics`) alongside the range total, so you get per-entity daily trends in ONE call instead of calling the tree once per day. Only `1` (daily) is supported. The daily series covers the same date range and uses the same source data as `metrics`, except `reach` on Meta and TikTok: the range total is the platform's de-duplicated value, so daily reach does not sum to it. See `dailyLevel` to control which levels carry it. (optional) 
            var dailyLevel = "campaign";  // string? | Which tree levels get the `daily[]` series when `timeIncrement=1`. `campaign` (default) attaches it on campaign nodes only — the common per-campaign-trend case, and the smallest payload. `adset` adds it on ad sets too; `ad` adds it on every ad in `ads[]` as well (heaviest — a long range × up to 100 ads per ad set). Scope with `campaignId` to keep `ad`-level responses small. Ignored when `timeIncrement` is unset. (optional)  (default to campaign)

            try
            {
                // Get campaign tree
                AdTreeResponse result = apiInstance.GetAdTree(page, limit, source, platform, status, adAccountId, pageId, accountId, profileId, campaignId, fromDate, toDate, hasDelivery, minSpend, sort, timeIncrement, dailyLevel);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetAdTree: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdTreeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get campaign tree
    ApiResponse<AdTreeResponse> response = apiInstance.GetAdTreeWithHttpInfo(page, limit, source, platform, status, adAccountId, pageId, accountId, profileId, campaignId, fromDate, toDate, hasDelivery, minSpend, sort, timeIncrement, dailyLevel);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetAdTreeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int?** | Campaigns per page | [optional] [default to 20] |
| **source** | **string?** | &#x60;all&#x60; (default) returns both Zernio-created ads and those discovered from the platform&#39;s ad manager — matches the web UI&#39;s default view. Pass &#x60;zernio&#x60; to restrict to isExternal&#x3D;false only. Status is NOT filtered by default — use the &#x60;status&#x60; param for that. | [optional] [default to all] |
| **platform** | **string?** |  | [optional]  |
| **status** | [**AdStatus?**](AdStatus?.md) | Filter by derived campaign status (post-aggregation) | [optional]  |
| **adAccountId** | **string?** | One or more platform ad account IDs to scope the tree to (agency profiles connect a whole Business Manager but a workspace usually cares about a subset). Comma-separate for multiple (&#x60;?adAccountId&#x3D;act_1,act_2,act_3&#x60;); single value keeps its old shape. Max 50 accounts per request; the plural aliases &#x60;adAccountIds&#x60; and &#x60;platformAdAccountIds&#x60; are rejected with a 400 to stop them from silently returning the unfiltered fleet. | [optional]  |
| **pageId** | **string?** | Meta only: Facebook Page ID. Prunes the tree to ads whose creative is backed by this Page — campaigns and ad sets with no ad on the Page drop out, and rolled-up metrics cover only the Page&#39;s ads. Mirrors the same filter on /v1/ads and /v1/ads/campaigns. | [optional]  |
| **accountId** | **string?** | Social account ID | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **campaignId** | **string?** | Restrict the tree to a single campaign by its platform campaign id (the id the platform assigns, e.g. Meta&#39;s numeric campaign id). Filters the campaign set itself, so it works regardless of account size and pagination — pass this when you already hold a campaign id instead of paging the tree to find it. Mirrors the &#x60;campaignId&#x60; filter on GET /v1/ads. | [optional]  |
| **fromDate** | **DateOnly?** | Start of the METRICS date range (YYYY-MM-DD). On its own it affects only the spend/impression numbers overlaid on each node, not which campaigns are returned — pass &#x60;hasDelivery&#x60; or &#x60;minSpend&#x60; to also filter the campaign set to this window. Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |
| **hasDelivery** | **bool?** | Return only campaigns that delivered between &#x60;fromDate&#x60; and &#x60;toDate&#x60; — spend above zero, or impressions served at zero spend. Unlike &#x60;status&#x60;, which reads a campaign&#39;s CURRENT state, this filters on what happened inside the window, so a campaign that spent then and is paused today is still returned. Filters the campaign set itself, so &#x60;pagination.total&#x60; counts only matching campaigns. | [optional]  |
| **minSpend** | **decimal?** | Return only campaigns whose spend between &#x60;fromDate&#x60; and &#x60;toDate&#x60; reaches this amount. Expressed in each campaign&#39;s OWN currency (the &#x60;currency&#x60; field on the campaign node): spend is stored per ad account in its native currency and one response can span several. Implies &#x60;hasDelivery&#x60;; &#x60;minSpend&#x3D;0&#x60; applies no filter. | [optional]  |
| **sort** | **string?** | Campaign-level sort order. &#x60;newest&#x60; (default) / &#x60;oldest&#x60; order by the campaign&#39;s newest-ad createdAt. &#x60;spend_desc&#x60; / &#x60;spend_asc&#x60; order by aggregated spend in the requested date range; campaigns with no spend land at the end. | [optional] [default to newest] |
| **timeIncrement** | **int?** | Set to &#x60;1&#x60; to also return a daily breakdown. Mirrors Meta Insights&#39; &#x60;time_increment&#x3D;1&#x60;: each node gains a &#x60;daily[]&#x60; array of per-day metrics (same fields as the aggregated &#x60;metrics&#x60;) alongside the range total, so you get per-entity daily trends in ONE call instead of calling the tree once per day. Only &#x60;1&#x60; (daily) is supported. The daily series covers the same date range and uses the same source data as &#x60;metrics&#x60;, except &#x60;reach&#x60; on Meta and TikTok: the range total is the platform&#39;s de-duplicated value, so daily reach does not sum to it. See &#x60;dailyLevel&#x60; to control which levels carry it. | [optional]  |
| **dailyLevel** | **string?** | Which tree levels get the &#x60;daily[]&#x60; series when &#x60;timeIncrement&#x3D;1&#x60;. &#x60;campaign&#x60; (default) attaches it on campaign nodes only — the common per-campaign-trend case, and the smallest payload. &#x60;adset&#x60; adds it on ad sets too; &#x60;ad&#x60; adds it on every ad in &#x60;ads[]&#x60; as well (heaviest — a long range × up to 100 ads per ad set). Scope with &#x60;campaignId&#x60; to keep &#x60;ad&#x60;-level responses small. Ignored when &#x60;timeIncrement&#x60; is unset. | [optional] [default to campaign] |

### Return type

[**AdTreeResponse**](AdTreeResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Nested campaign tree with pagination |  -  |
| **202** | Historical data is incomplete and backfill remains pending. |  * Retry-After -  <br>  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadstimeline"></a>
# **GetAdsTimeline**
> AdsTimelineResponse GetAdsTimeline (string accountId, string? adAccountId = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? platform = null)

Get daily account metrics

Returns daily aggregate metrics across all ads in a SocialAccount as a single time series — one row per calendar day in the requested range. Use this for dashboards that draw a daily-spend or daily-conversions chart, instead of calling `/v1/ads/tree` once per day.  `accountId` is required. The lookup is sibling-expanded so passing the `metaads` ID also includes ads under the linked `facebook` / `instagram` posting account (and vice-versa) — same convention as `/v1/ads/tree` and `/v1/ads`.  Date range defaults to the last 90 days. Capped at 730 days. Ranges older than the ingested history return a `202` immediately with the covered part and `backfillPending: true` while the rest is backfilled in the background; repeat the request shortly until it returns 200 with full data. 

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
    public class GetAdsTimelineExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var accountId = "accountId_example";  // string | Social account ID. Sibling-expanded to its linked posting↔ads pair.
            var adAccountId = "adAccountId_example";  // string? | Optional platform-native ad account ID (e.g. Meta `act_…`, TikTok advertiser ID). Use when the connection wraps multiple platform ad accounts and the chart should show one only. Note: rows ingested before 2026-05-13 don't carry this column; the recurring 7-day re-sync repopulates them naturally. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Inclusive start of metrics range (YYYY-MM-DD). Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Inclusive end of metrics range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 
            var platform = "facebook";  // string? | Restrict to one platform. (optional) 

            try
            {
                // Get daily account metrics
                AdsTimelineResponse result = apiInstance.GetAdsTimeline(accountId, adAccountId, fromDate, toDate, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetAdsTimeline: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdsTimelineWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get daily account metrics
    ApiResponse<AdsTimelineResponse> response = apiInstance.GetAdsTimelineWithHttpInfo(accountId, adAccountId, fromDate, toDate, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetAdsTimelineWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Social account ID. Sibling-expanded to its linked posting↔ads pair. |  |
| **adAccountId** | **string?** | Optional platform-native ad account ID (e.g. Meta &#x60;act_…&#x60;, TikTok advertiser ID). Use when the connection wraps multiple platform ad accounts and the chart should show one only. Note: rows ingested before 2026-05-13 don&#39;t carry this column; the recurring 7-day re-sync repopulates them naturally. | [optional]  |
| **fromDate** | **DateOnly?** | Inclusive start of metrics range (YYYY-MM-DD). Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | Inclusive end of metrics range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |
| **platform** | **string?** | Restrict to one platform. | [optional]  |

### Return type

[**AdsTimelineResponse**](AdsTimelineResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Daily time series of aggregate metrics. Empty &#x60;rows&#x60; means the account has no ad activity in the range. |  -  |
| **202** | Historical data is incomplete and backfill remains pending. |  * Retry-After -  <br>  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcampaigns"></a>
# **ListAdCampaigns**
> ListAdCampaigns200Response ListAdCampaigns (bool? includeEmpty = null, int? page = null, int? limit = null, string? source = null, string? platform = null, AdStatus? status = null, string? adAccountId = null, string? pageId = null, string? accountId = null, string? profileId = null, DateOnly? fromDate = null, DateOnly? toDate = null, bool? hasDelivery = null, decimal? minSpend = null)

List campaigns

Returns campaigns as virtual aggregations over ad documents grouped by platform campaign ID. Metrics (spend, impressions, clicks, etc.) are summed across all ads in each campaign. Campaign status is derived from child ad statuses (active > pending_review > paused > error > completed > cancelled > rejected). 

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
    public class ListAdCampaignsExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var includeEmpty = true;  // bool? | Meta only. Campaign reads aggregate over ad documents, so a campaign with ZERO ads is normally invisible here — the state the two-step create (campaign, then ads via `existingCampaignId`) leaves behind whenever Meta rejects the ad step. Set true to list those too, with `adCount: 0` and zeroed metrics. Requires `accountId` and `adAccountId`, since an empty campaign has no ad row to resolve a token or ad account from. (optional) 
            var page = 1;  // int? | Page number (1-based) (optional)  (default to 1)
            var limit = 20;  // int? |  (optional)  (default to 20)
            var source = "zernio";  // string? | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager — matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default — use the `status` param for that. (optional)  (default to all)
            var platform = "facebook";  // string? |  (optional) 
            var status = new AdStatus?(); // AdStatus? | Filter by derived campaign status (post-aggregation) (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (e.g. act_123 for Meta) (optional) 
            var pageId = "pageId_example";  // string? | Meta only: Facebook Page ID. Campaigns have no Page of their own, so this keeps campaigns having at least one ad backed by this Page, with adCount and metrics computed over those ads only. Mirrors the same filter on /v1/ads and /v1/ads/tree. (optional) 
            var accountId = "accountId_example";  // string? | Social account ID (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of metrics date range (YYYY-MM-DD, inclusive). Defaults to 90 days ago when both date params are omitted. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of metrics date range (YYYY-MM-DD, inclusive). Defaults to today. Max 730-day range. (optional) 
            var hasDelivery = true;  // bool? | Return only campaigns that delivered between `fromDate` and `toDate` — spend above zero, or impressions served at zero spend. Unlike `status`, which reads a campaign's CURRENT state, this filters on what happened inside the window. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. Mirrors the same filter on /v1/ads/tree. (optional) 
            var minSpend = 8.14D;  // decimal? | Return only campaigns whose spend between `fromDate` and `toDate` reaches this amount, in each campaign's OWN currency (the `currency` field on the campaign). Implies `hasDelivery`; `minSpend=0` applies no filter. Mirrors the same filter on /v1/ads/tree. (optional) 

            try
            {
                // List campaigns
                ListAdCampaigns200Response result = apiInstance.ListAdCampaigns(includeEmpty, page, limit, source, platform, status, adAccountId, pageId, accountId, profileId, fromDate, toDate, hasDelivery, minSpend);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListAdCampaigns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdCampaignsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaigns
    ApiResponse<ListAdCampaigns200Response> response = apiInstance.ListAdCampaignsWithHttpInfo(includeEmpty, page, limit, source, platform, status, adAccountId, pageId, accountId, profileId, fromDate, toDate, hasDelivery, minSpend);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListAdCampaignsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **includeEmpty** | **bool?** | Meta only. Campaign reads aggregate over ad documents, so a campaign with ZERO ads is normally invisible here — the state the two-step create (campaign, then ads via &#x60;existingCampaignId&#x60;) leaves behind whenever Meta rejects the ad step. Set true to list those too, with &#x60;adCount: 0&#x60; and zeroed metrics. Requires &#x60;accountId&#x60; and &#x60;adAccountId&#x60;, since an empty campaign has no ad row to resolve a token or ad account from. | [optional]  |
| **page** | **int?** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int?** |  | [optional] [default to 20] |
| **source** | **string?** | &#x60;all&#x60; (default) returns both Zernio-created ads and those discovered from the platform&#39;s ad manager — matches the web UI&#39;s default view. Pass &#x60;zernio&#x60; to restrict to isExternal&#x3D;false only. Status is NOT filtered by default — use the &#x60;status&#x60; param for that. | [optional] [default to all] |
| **platform** | **string?** |  | [optional]  |
| **status** | [**AdStatus?**](AdStatus?.md) | Filter by derived campaign status (post-aggregation) | [optional]  |
| **adAccountId** | **string?** | Platform ad account ID (e.g. act_123 for Meta) | [optional]  |
| **pageId** | **string?** | Meta only: Facebook Page ID. Campaigns have no Page of their own, so this keeps campaigns having at least one ad backed by this Page, with adCount and metrics computed over those ads only. Mirrors the same filter on /v1/ads and /v1/ads/tree. | [optional]  |
| **accountId** | **string?** | Social account ID | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **fromDate** | **DateOnly?** | Start of metrics date range (YYYY-MM-DD, inclusive). Defaults to 90 days ago when both date params are omitted. | [optional]  |
| **toDate** | **DateOnly?** | End of metrics date range (YYYY-MM-DD, inclusive). Defaults to today. Max 730-day range. | [optional]  |
| **hasDelivery** | **bool?** | Return only campaigns that delivered between &#x60;fromDate&#x60; and &#x60;toDate&#x60; — spend above zero, or impressions served at zero spend. Unlike &#x60;status&#x60;, which reads a campaign&#39;s CURRENT state, this filters on what happened inside the window. Filters the campaign set itself, so &#x60;pagination.total&#x60; counts only matching campaigns. Mirrors the same filter on /v1/ads/tree. | [optional]  |
| **minSpend** | **decimal?** | Return only campaigns whose spend between &#x60;fromDate&#x60; and &#x60;toDate&#x60; reaches this amount, in each campaign&#39;s OWN currency (the &#x60;currency&#x60; field on the campaign). Implies &#x60;hasDelivery&#x60;; &#x60;minSpend&#x3D;0&#x60; applies no filter. Mirrors the same filter on /v1/ads/tree. | [optional]  |

### Return type

[**ListAdCampaigns200Response**](ListAdCampaigns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated campaigns |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadkeywords"></a>
# **ListAdKeywords**
> ListAdKeywords200Response ListAdKeywords (int? page = null, int? limit = null, string? accountId = null, string? adAccountId = null, string? profileId = null, string? campaignId = null, string? adSetId = null, string? status = null, string? matchType = null, bool? negative = null, string? search = null)

List Search keywords

Returns the Google Search keyword criteria (positive and negative) synced from connected Google Ads accounts, one row per ad-group keyword. Refreshed about once a week per Google Ads customer (the keyword sweep rides the ads discovery pass on a slower slot, to stay inside Google's shared daily API quota), so keywords added on Google can take several days to appear. A customer synced for the first time is populated on the next discovery pass rather than waiting for its weekly slot, and connecting an account or triggering a manual sync refreshes it immediately. Campaign-level negative keywords are not included; only ad-group-level criteria are. 

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
    public class ListAdKeywordsExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var page = 1;  // int? | Page number (1-based) (optional)  (default to 1)
            var limit = 50;  // int? |  (optional)  (default to 50)
            var accountId = "accountId_example";  // string? | Social account ID (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID). Mirrors the same filter on /v1/ads. (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var campaignId = "campaignId_example";  // string? | Platform campaign ID (optional) 
            var adSetId = "adSetId_example";  // string? | Platform ad group ID (Google ad group) (optional) 
            var status = "active";  // string? | Keyword criterion status (optional) 
            var matchType = "exact";  // string? |  (optional) 
            var negative = true;  // bool? | true = negative keywords only, false = positive only. Omit for both. (optional) 
            var search = "search_example";  // string? | Case-insensitive substring match on the keyword text (optional) 

            try
            {
                // List Search keywords
                ListAdKeywords200Response result = apiInstance.ListAdKeywords(page, limit, accountId, adAccountId, profileId, campaignId, adSetId, status, matchType, negative, search);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListAdKeywords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdKeywordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Search keywords
    ApiResponse<ListAdKeywords200Response> response = apiInstance.ListAdKeywordsWithHttpInfo(page, limit, accountId, adAccountId, profileId, campaignId, adSetId, status, matchType, negative, search);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListAdKeywordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int?** |  | [optional] [default to 50] |
| **accountId** | **string?** | Social account ID | [optional]  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID). Mirrors the same filter on /v1/ads. | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **campaignId** | **string?** | Platform campaign ID | [optional]  |
| **adSetId** | **string?** | Platform ad group ID (Google ad group) | [optional]  |
| **status** | **string?** | Keyword criterion status | [optional]  |
| **matchType** | **string?** |  | [optional]  |
| **negative** | **bool?** | true &#x3D; negative keywords only, false &#x3D; positive only. Omit for both. | [optional]  |
| **search** | **string?** | Case-insensitive substring match on the keyword text | [optional]  |

### Return type

[**ListAdKeywords200Response**](ListAdKeywords200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated keywords |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listads"></a>
# **ListAds**
> AdsListResponse ListAds (int? page = null, int? limit = null, string? source = null, AdStatus? status = null, string? platform = null, string? accountId = null, string? adAccountId = null, string? pageId = null, string? profileId = null, string? campaignId = null, string? platformAdId = null, string? effectiveObjectStoryId = null, string? effectiveInstagramMediaId = null, DateOnly? fromDate = null, DateOnly? toDate = null)

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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var page = 1;  // int? | Page number (1-based) (optional)  (default to 1)
            var limit = 50;  // int? |  (optional)  (default to 50)
            var source = "zernio";  // string? | all (default) = Zernio-created + platform-discovered ads. zernio = restrict to Zernio-created only. (optional)  (default to all)
            var status = new AdStatus?(); // AdStatus? |  (optional) 
            var platform = "facebook";  // string? |  (optional) 
            var accountId = "accountId_example";  // string? | Social account ID (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. (optional) 
            var pageId = "pageId_example";  // string? | Meta only: Facebook Page ID. Returns only ads whose creative is backed by this Page (a Meta ad account serves ads for every Page in the Business Manager). Matches each ad's `creative.pageId`; ads with no page signal (rare IG-only creatives) never match. Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. (optional) 
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
                AdsListResponse result = apiInstance.ListAds(page, limit, source, status, platform, accountId, adAccountId, pageId, profileId, campaignId, platformAdId, effectiveObjectStoryId, effectiveInstagramMediaId, fromDate, toDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListAds: " + e.Message);
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
    ApiResponse<AdsListResponse> response = apiInstance.ListAdsWithHttpInfo(page, limit, source, status, platform, accountId, adAccountId, pageId, profileId, campaignId, platformAdId, effectiveObjectStoryId, effectiveInstagramMediaId, fromDate, toDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListAdsWithHttpInfo: " + e.Message);
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
| **pageId** | **string?** | Meta only: Facebook Page ID. Returns only ads whose creative is backed by this Page (a Meta ad account serves ads for every Page in the Business Manager). Matches each ad&#39;s &#x60;creative.pageId&#x60;; ads with no page signal (rare IG-only creatives) never match. Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **campaignId** | **string?** | Platform campaign ID (filter ads within a campaign) | [optional]  |
| **platformAdId** | **string?** | Meta ad ID. Returns the ad with this platform-side ad ID. | [optional]  |
| **effectiveObjectStoryId** | **string?** | Facebook &#x60;{pageId}_{postId}&#x60; of the post the ad&#39;s engagement lives on (Meta &#x60;effective_object_story_id&#x60;). Use to map a Business-Manager-visible post back to the Zernio ad. | [optional]  |
| **effectiveInstagramMediaId** | **string?** | Instagram media ID of the boosted post (Meta &#x60;effective_instagram_media_id&#x60;). Use to map a Business-Manager-visible IG post back to the Zernio ad. | [optional]  |
| **fromDate** | **DateOnly?** | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |

### Return type

[**AdsListResponse**](AdsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated ads |  -  |
| **202** | Historical data is incomplete and backfill remains pending. |  * Retry-After -  <br>  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatead"></a>
# **UpdateAd**
> UpdateAd200Response UpdateAd (string adId, UpdateAdRequest updateAdRequest)

Update ad

Patch one or more fields on an ad. Status, budget, targeting, and creative changes are propagated to the platform.  Per-platform support: - **Meta** (Facebook + Instagram): all fields supported. - **TikTok**: status, budget, targeting (via `/v2/adgroup/update/`), and creative   (via `/v2/ad/update/` patch-style — `headline` is ignored, `body` becomes `ad_text`). - **Google**: status, budget, and KEYWORD edits via `targeting.keywords` /   `targeting.negativeKeywords` — each list you send becomes the FULL new set of its   kind on the ad group (criteria not in the list are removed); a kind left out is   untouched. Any other `targeting` field returns 400: Google cannot mutate broad   targeting post-create without recreating the campaign. `creative` returns 501. - **LinkedIn**: status, budget, targeting (geo countries only, applied to the   LinkedIn Campaign via PARTIAL_UPDATE), and creative (uploads new media, creates a   replacement inline creative on the same campaign, pauses the old one). - **Pinterest / X / OpenAI Ads**: status + budget only. Sending   `targeting` or `creative` returns 501 with code `unsupported_platform_operation`.   OpenAI Ads budget is lifetime-only (see `budget.type` below). 

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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAd: " + e.Message);
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
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdWithHttpInfo: " + e.Message);
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
| **501** | targeting or creative not supported on the platform (supported on Meta, TikTok, and LinkedIn) |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadcampaign"></a>
# **UpdateAdCampaign**
> UpdateAdCampaign200Response UpdateAdCampaign (string campaignId, UpdateAdCampaignRequest updateAdCampaignRequest)

Update a campaign

Campaign-level edits. Send at least one of `budget`, `bidStrategy`, `name` or `platformSpecificData`. An unsupported field is always an error, never a silent drop.  | Body field | Meta | Google | Others | |- --|- --|- --|- --| | `bidStrategy` | Yes | Yes | 501 | | `bidAmount`, `roasAverageFloor` | 400 — ad-set level | Yes | 400 | | `budget` (CBO; ABO returns 409) | Yes | 501 | 501 | | `name` | Yes | 501 | 501 | | `platformSpecificData.spendCap` | Yes | 400 | 400 | | `accountId` (empty campaigns) | Yes | - | - |  Google maps the shared enum onto its own strategies: `LOWEST_COST_WITHOUT_CAP` to Maximize Clicks, `LOWEST_COST_WITH_BID_CAP` to Maximize Clicks with a max CPC (`bidAmount`), `COST_CAP` to Target CPA (`bidAmount`), `LOWEST_COST_WITH_MIN_ROAS` to Target ROAS (`roasAverageFloor`). A campaign on a PORTFOLIO bidding strategy is rejected: detach it in Google Ads first, since it is shared across campaigns.  `accountId` forwards the update straight to Meta for a campaign with zero ads, which would otherwise 404; the response then carries `updated: 0`. 

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
    public class UpdateAdCampaignExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Platform campaign ID
            var updateAdCampaignRequest = new UpdateAdCampaignRequest(); // UpdateAdCampaignRequest | 

            try
            {
                // Update a campaign
                UpdateAdCampaign200Response result = apiInstance.UpdateAdCampaign(campaignId, updateAdCampaignRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAdCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a campaign
    ApiResponse<UpdateAdCampaign200Response> response = apiInstance.UpdateAdCampaignWithHttpInfo(campaignId, updateAdCampaignRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Platform campaign ID |  |
| **updateAdCampaignRequest** | [**UpdateAdCampaignRequest**](UpdateAdCampaignRequest.md) |  |  |

### Return type

[**UpdateAdCampaign200Response**](UpdateAdCampaign200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign updated |  -  |
| **400** | Invalid input, or a field the resolved platform does not support at the campaign level (see the support table) |  -  |
| **401** | Unauthorized |  -  |
| **404** | Campaign not found |  -  |
| **409** | Campaign is ABO — route to /v1/ads/ad-sets/{adSetId} instead |  -  |
| **501** | Operation not supported on this platform |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadcampaignstatus"></a>
# **UpdateAdCampaignStatus**
> UpdateAdCampaignStatus200Response UpdateAdCampaignStatus (string campaignId, UpdateAdCampaignStatusRequest updateAdCampaignStatusRequest)

Pause or resume a campaign

Writes the campaign's own on/off switch, then lets the platform cascade delivery to its ad sets and ads. Makes one platform API call, not one per ad.  The switch is always written, whatever delivery status the ads underneath report: an ad still in review does not block resuming its campaign. The echoed `status` is the confirmation that it landed.  `updated` / `skipped` describe only the ads whose own stored status CHANGED alongside it, so `updated: 0` is a normal successful response, not a no-op. Ads are skipped when they are in a terminal status (rejected, completed, cancelled), already in the target state, or switched on but not yet delivering — the last group keeps its `pending_review` / `error` status until the platform reports what it became. `skippedReasons` names which case applies.  On Meta this flips the campaign only. An ad set paused in its own right stays paused, so pair this with PUT /v1/ads/ad-sets/{adSetId}/status when you also need the ad set switched back on. 

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
    public class UpdateAdCampaignStatusExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var campaignId = "campaignId_example";  // string | Platform campaign ID
            var updateAdCampaignStatusRequest = new UpdateAdCampaignStatusRequest(); // UpdateAdCampaignStatusRequest | 

            try
            {
                // Pause or resume a campaign
                UpdateAdCampaignStatus200Response result = apiInstance.UpdateAdCampaignStatus(campaignId, updateAdCampaignStatusRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAdCampaignStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdCampaignStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause or resume a campaign
    ApiResponse<UpdateAdCampaignStatus200Response> response = apiInstance.UpdateAdCampaignStatusWithHttpInfo(campaignId, updateAdCampaignStatusRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdCampaignStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Platform campaign ID |  |
| **updateAdCampaignStatusRequest** | [**UpdateAdCampaignStatusRequest**](UpdateAdCampaignStatusRequest.md) |  |  |

### Return type

[**UpdateAdCampaignStatus200Response**](UpdateAdCampaignStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign status updated |  -  |
| **400** | Invalid input or campaign spans multiple social accounts |  -  |
| **401** | Unauthorized |  -  |
| **404** | No ads found for this campaign |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadset"></a>
# **UpdateAdSet**
> UpdateAdSet200Response UpdateAdSet (string adSetId, UpdateAdSetRequest updateAdSetRequest)

Update an ad set

Ad-set-level writes. Use this for ABO budget updates, ad-set-scoped pause/resume, bid-strategy edits, Meta value-rule-set attach/detach, and Meta-only post-launch delivery settings via `platformSpecificData`. At least one updatable field is required.  Value rule sets (Meta only, see `/v1/ads/value-rule-sets`): - ATTACH or REPLACE: send `valueRuleSetId`. Attachment is driven by the id's   presence, so `valueRulesApplied: true` is optional. Sending a different id   replaces the previous association; there is no separate replace call. - DETACH: send `valueRulesApplied: false` and OMIT `valueRuleSetId`. - Sending `valueRulesApplied: false` TOGETHER with `valueRuleSetId` returns 400   `mutually_exclusive_fields`. This is deliberate: Meta attaches the rule set   whenever `value_rule_set_id` is present, even with `value_rules_applied` false,   so echoing stored state while asking to detach would silently keep the bid   adjustments live. - Eligibility: only ad sets on `LOWEST_COST_WITHOUT_CAP` or `COST_CAP`. Meta   rejects the rest server-side. - Read back with `GET /v1/ads/ad-sets/{adSetId}?fields=value_rule_set_id`. Meta   does not document `value_rules_applied` as a readable ad-set field, so the   boolean cannot be read back.  Bid strategy compatibility (per Meta's spec): - `LOWEST_COST_WITHOUT_CAP`: no `bidAmount`, no `roasAverageFloor`. - `LOWEST_COST_WITH_BID_CAP` / `COST_CAP`: `bidAmount` REQUIRED (whole currency units). - `LOWEST_COST_WITH_MIN_ROAS`: `roasAverageFloor` REQUIRED (decimal multiplier, e.g. 2.0 = 2.0x ROAS). - Meta only: send `bidAmount` WITHOUT `bidStrategy` to change the cap amount on an ad set   under a COST_CAP / LOWEST_COST_WITH_BID_CAP parent campaign, leaving the strategy itself   (inherited from the campaign) untouched. `roasAverageFloor` without `bidStrategy` is   rejected (it has no meaning outside LOWEST_COST_WITH_MIN_ROAS).  Delivery settings are validated by Meta against the campaign objective; incompatible combinations (e.g. a billingEvent the optimization goal doesn't allow) surface as 400s from Meta.  When updating `budget` on an ABO campaign: if the parent campaign is CBO, the response is 409 with code BUDGET_LEVEL_MISMATCH — route to PUT /v1/ads/campaigns/{campaignId} instead. 

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
    public class UpdateAdSetExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adSetId = "adSetId_example";  // string | Platform ad set ID
            var updateAdSetRequest = new UpdateAdSetRequest(); // UpdateAdSetRequest | 

            try
            {
                // Update an ad set
                UpdateAdSet200Response result = apiInstance.UpdateAdSet(adSetId, updateAdSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAdSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an ad set
    ApiResponse<UpdateAdSet200Response> response = apiInstance.UpdateAdSetWithHttpInfo(adSetId, updateAdSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Platform ad set ID |  |
| **updateAdSetRequest** | [**UpdateAdSetRequest**](UpdateAdSetRequest.md) |  |  |

### Return type

[**UpdateAdSet200Response**](UpdateAdSet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad set updated |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad set not found |  -  |
| **409** | Campaign is CBO — route to /v1/ads/campaigns/{campaignId} instead |  -  |
| **422** | bidStrategy is LOWEST_COST_WITH_MIN_ROAS on OpenAI (unsupported: no ROAS-based bidding) |  -  |
| **501** | bidStrategy not supported on the platform (Meta, TikTok, and OpenAI only) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadsetstatus"></a>
# **UpdateAdSetStatus**
> UpdateAdSetStatus200Response UpdateAdSetStatus (string adSetId, UpdateAdCampaignStatusRequest updateAdCampaignStatusRequest)

Pause or resume a single ad set

Ad-set-scoped pause/resume (doesn't touch sibling ad sets). Thin wrapper over PUT /v1/ads/ad-sets/{adSetId} for callers that only want the status toggle and prefer a symmetric URL to /v1/ads/campaigns/{campaignId}/status.  On Meta and LinkedIn this writes the ad set's own on/off switch (Meta: `configured_status`), whatever delivery status its ads report — an ad still in review does not block resuming its ad set. The echoed `status` is the confirmation that it landed. Where the platform has no ad-set switch (TikTok and others) the toggle is emulated by flipping the child ads; a call with no actionable ad then writes nothing and returns a `message` with no `status`.  `updated` / `skipped` describe only the ads whose own stored status CHANGED alongside the switch, so `updated: 0` is a normal successful response. See `skippedReasons` for which of the three cases applies (terminal, already in the target state, or switched on but not yet delivering).  A campaign created paused needs its campaign resumed as well: pair this with PUT /v1/ads/campaigns/{campaignId}/status. 

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
    public class UpdateAdSetStatusExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adSetId = "adSetId_example";  // string | Platform ad set ID
            var updateAdCampaignStatusRequest = new UpdateAdCampaignStatusRequest(); // UpdateAdCampaignStatusRequest | 

            try
            {
                // Pause or resume a single ad set
                UpdateAdSetStatus200Response result = apiInstance.UpdateAdSetStatus(adSetId, updateAdCampaignStatusRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAdSetStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdSetStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause or resume a single ad set
    ApiResponse<UpdateAdSetStatus200Response> response = apiInstance.UpdateAdSetStatusWithHttpInfo(adSetId, updateAdCampaignStatusRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdSetStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Platform ad set ID |  |
| **updateAdCampaignStatusRequest** | [**UpdateAdCampaignStatusRequest**](UpdateAdCampaignStatusRequest.md) |  |  |

### Return type

[**UpdateAdSetStatus200Response**](UpdateAdSetStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad set status updated |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad set not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadstatus"></a>
# **UpdateAdStatus**
> UpdateAdStatus200Response UpdateAdStatus (string adId, UpdateAdStatusRequest updateAdStatusRequest)

Pause or resume a single ad

Ad-scoped pause/resume — touches ONLY this ad, never its parent ad set or campaign (so sibling ads keep running). Thin wrapper over the `status` field of PUT /v1/ads/{adId}, for callers that want a URL symmetric to /v1/ads/campaigns/{campaignId}/status and /v1/ads/ad-sets/{adSetId}/status.  `{adId}` accepts the same identifier dialects as GET/PUT /v1/ads/{adId} (Zernio hex `_id`, Meta numeric `platformAdId`, or the creative's effective story/media IDs). `platform` is inferred from the ad, so it's not required in the body. Ads in terminal statuses (rejected, completed, cancelled) and no-op flips (already in the target state) are skipped. 

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
    public class UpdateAdStatusExample
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
            var apiInstance = new AdCampaignsApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | Zernio `_id` (hex), Meta `platformAdId` (numeric), or one of the creative's effective story/media IDs.
            var updateAdStatusRequest = new UpdateAdStatusRequest(); // UpdateAdStatusRequest | 

            try
            {
                // Pause or resume a single ad
                UpdateAdStatus200Response result = apiInstance.UpdateAdStatus(adId, updateAdStatusRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAdStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause or resume a single ad
    ApiResponse<UpdateAdStatus200Response> response = apiInstance.UpdateAdStatusWithHttpInfo(adId, updateAdStatusRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Zernio &#x60;_id&#x60; (hex), Meta &#x60;platformAdId&#x60; (numeric), or one of the creative&#39;s effective story/media IDs. |  |
| **updateAdStatusRequest** | [**UpdateAdStatusRequest**](UpdateAdStatusRequest.md) |  |  |

### Return type

[**UpdateAdStatus200Response**](UpdateAdStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad status updated (or skipped when no change was needed) |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **404** | Ad not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

