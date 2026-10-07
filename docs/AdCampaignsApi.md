# Zernio.Api.AdCampaignsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddAdKeywords**](AdCampaignsApi.md#addadkeywords) | **POST** /v1/ads/keywords | Add Search ad-group keywords |
| [**ApplyGoogleRecommendations**](AdCampaignsApi.md#applygooglerecommendations) | **POST** /v1/ads/recommendations/apply | Apply Google Ads recommendations |
| [**AttachAdGroupAssets**](AdCampaignsApi.md#attachadgroupassets) | **POST** /v1/ads/ad-sets/{adSetId}/assets | Attach ad-group assets |
| [**AttachCampaignAssets**](AdCampaignsApi.md#attachcampaignassets) | **POST** /v1/ads/campaigns/{campaignId}/assets | Attach campaign assets |
| [**BoostPost**](AdCampaignsApi.md#boostpost) | **POST** /v1/ads/boost | Boost post as ad |
| [**BulkUpdateAdCampaignStatus**](AdCampaignsApi.md#bulkupdateadcampaignstatus) | **POST** /v1/ads/campaigns/bulk-status | Pause or resume many campaigns |
| [**CreateAdCampaign**](AdCampaignsApi.md#createadcampaign) | **POST** /v1/ads/campaigns | Create a standalone campaign |
| [**CreateAdSet**](AdCampaignsApi.md#createadset) | **POST** /v1/ads/ad-sets | Create a standalone ad group |
| [**CreateBidStrategy**](AdCampaignsApi.md#createbidstrategy) | **POST** /v1/ads/bid-strategies | Create portfolio bid strategy |
| [**CreateGoogleAssetGroup**](AdCampaignsApi.md#creategoogleassetgroup) | **POST** /v1/ads/campaigns/{campaignId}/asset-groups | Create a Performance Max asset group |
| [**CreateSharedBudget**](AdCampaignsApi.md#createsharedbudget) | **POST** /v1/ads/shared-budgets | Create a shared budget |
| [**CreateStandaloneAd**](AdCampaignsApi.md#createstandalonead) | **POST** /v1/ads/create | Create standalone ad |
| [**DeleteAd**](AdCampaignsApi.md#deletead) | **DELETE** /v1/ads/{adId} | Cancel an ad |
| [**DeleteAdCampaign**](AdCampaignsApi.md#deleteadcampaign) | **DELETE** /v1/ads/campaigns/{campaignId} | Delete a campaign |
| [**DeleteAdSet**](AdCampaignsApi.md#deleteadset) | **DELETE** /v1/ads/ad-sets/{adSetId} | Delete an ad set |
| [**DismissGoogleRecommendations**](AdCampaignsApi.md#dismissgooglerecommendations) | **POST** /v1/ads/recommendations/dismiss | Dismiss Google Ads recommendations |
| [**DuplicateAd**](AdCampaignsApi.md#duplicatead) | **POST** /v1/ads/{adId}/duplicate | Duplicate an ad |
| [**DuplicateAdCampaign**](AdCampaignsApi.md#duplicateadcampaign) | **POST** /v1/ads/campaigns/{campaignId}/duplicate | Duplicate a campaign |
| [**DuplicateAdSet**](AdCampaignsApi.md#duplicateadset) | **POST** /v1/ads/ad-sets/{adSetId}/duplicate | Duplicate an ad set |
| [**EditGoogleAssetGroupAssets**](AdCampaignsApi.md#editgoogleassetgroupassets) | **POST** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId}/assets | Link or unlink asset group assets |
| [**GetAd**](AdCampaignsApi.md#getad) | **GET** /v1/ads/{adId} | Get ad details |
| [**GetAdCampaignDetails**](AdCampaignsApi.md#getadcampaigndetails) | **GET** /v1/ads/campaigns/{campaignId} | Get live campaign details |
| [**GetAdReview**](AdCampaignsApi.md#getadreview) | **GET** /v1/ads/{adId}/review | Read the platform&#39;s review verdict for an ad |
| [**GetAdSetDetails**](AdCampaignsApi.md#getadsetdetails) | **GET** /v1/ads/ad-sets/{adSetId} | Get live ad-set details |
| [**GetAdTree**](AdCampaignsApi.md#getadtree) | **GET** /v1/ads/tree | Get campaign tree |
| [**GetAdsTimeline**](AdCampaignsApi.md#getadstimeline) | **GET** /v1/ads/timeline | Get daily account metrics |
| [**GetCampaignAdSchedule**](AdCampaignsApi.md#getcampaignadschedule) | **GET** /v1/ads/campaigns/{campaignId}/ad-schedule | Read a campaign&#39;s ad schedule (dayparting) |
| [**GetCampaignBidding**](AdCampaignsApi.md#getcampaignbidding) | **GET** /v1/ads/campaigns/{campaignId}/bidding | Read a campaign&#39;s current bidding |
| [**GetCampaignConversionGoals**](AdCampaignsApi.md#getcampaignconversiongoals) | **GET** /v1/ads/campaigns/{campaignId}/conversion-goals | Get campaign conversion goals |
| [**GetCampaignTargeting**](AdCampaignsApi.md#getcampaigntargeting) | **GET** /v1/ads/campaigns/{campaignId}/targeting | Read a Google campaign&#39;s device, location, excluded location, and language targeting |
| [**GetGoogleAssetGroup**](AdCampaignsApi.md#getgoogleassetgroup) | **GET** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId} | Get a Performance Max asset group |
| [**ListAdCampaigns**](AdCampaignsApi.md#listadcampaigns) | **GET** /v1/ads/campaigns | List campaigns |
| [**ListAdGroupAssets**](AdCampaignsApi.md#listadgroupassets) | **GET** /v1/ads/ad-sets/{adSetId}/assets | List ad-group assets |
| [**ListAdKeywords**](AdCampaignsApi.md#listadkeywords) | **GET** /v1/ads/keywords | List Search keywords |
| [**ListAdSets**](AdCampaignsApi.md#listadsets) | **GET** /v1/ads/ad-sets | List ad sets |
| [**ListAds**](AdCampaignsApi.md#listads) | **GET** /v1/ads | List ads |
| [**ListBidStrategies**](AdCampaignsApi.md#listbidstrategies) | **GET** /v1/ads/bid-strategies | List portfolio bid strategies |
| [**ListCampaignAssets**](AdCampaignsApi.md#listcampaignassets) | **GET** /v1/ads/campaigns/{campaignId}/assets | List campaign assets |
| [**ListCampaignNegativeKeywordLists**](AdCampaignsApi.md#listcampaignnegativekeywordlists) | **GET** /v1/ads/campaigns/{campaignId}/negative-keyword-lists | List campaign negative lists |
| [**ListCampaignNegativeKeywords**](AdCampaignsApi.md#listcampaignnegativekeywords) | **GET** /v1/ads/campaigns/{campaignId}/negative-keywords | List campaign-level negative keywords |
| [**ListGoogleAssetGroups**](AdCampaignsApi.md#listgoogleassetgroups) | **GET** /v1/ads/campaigns/{campaignId}/asset-groups | List Performance Max asset groups |
| [**ListGoogleRecommendations**](AdCampaignsApi.md#listgooglerecommendations) | **GET** /v1/ads/recommendations | List Google Ads recommendations |
| [**ListSharedBudgets**](AdCampaignsApi.md#listsharedbudgets) | **GET** /v1/ads/shared-budgets | List shared budgets |
| [**RemoveAdGroupAssets**](AdCampaignsApi.md#removeadgroupassets) | **DELETE** /v1/ads/ad-sets/{adSetId}/assets | Remove ad-group assets |
| [**RemoveAdKeyword**](AdCampaignsApi.md#removeadkeyword) | **DELETE** /v1/ads/keywords/{keywordId} | Remove a Search keyword |
| [**RemoveCampaignAssets**](AdCampaignsApi.md#removecampaignassets) | **DELETE** /v1/ads/campaigns/{campaignId}/assets | Remove campaign assets |
| [**RemoveGoogleAssetGroup**](AdCampaignsApi.md#removegoogleassetgroup) | **DELETE** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId} | Remove a Performance Max asset group |
| [**ReplaceCampaignNegativeKeywordLists**](AdCampaignsApi.md#replacecampaignnegativekeywordlists) | **PUT** /v1/ads/campaigns/{campaignId}/negative-keyword-lists | Replace campaign negative lists |
| [**ReplaceCampaignNegativeKeywords**](AdCampaignsApi.md#replacecampaignnegativekeywords) | **PUT** /v1/ads/campaigns/{campaignId}/negative-keywords | Replace campaign-level negative keywords |
| [**ReplaceGoogleListingGroupFilters**](AdCampaignsApi.md#replacegooglelistinggroupfilters) | **PUT** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId}/listing-group-filters | Replace an asset group&#39;s listing-group tree |
| [**UpdateAd**](AdCampaignsApi.md#updatead) | **PUT** /v1/ads/{adId} | Update ad |
| [**UpdateAdCampaign**](AdCampaignsApi.md#updateadcampaign) | **PUT** /v1/ads/campaigns/{campaignId} | Update a campaign |
| [**UpdateAdCampaignStatus**](AdCampaignsApi.md#updateadcampaignstatus) | **PUT** /v1/ads/campaigns/{campaignId}/status | Pause or resume a campaign |
| [**UpdateAdGroupAssets**](AdCampaignsApi.md#updateadgroupassets) | **PUT** /v1/ads/ad-sets/{adSetId}/assets | Update ad-group assets |
| [**UpdateAdKeyword**](AdCampaignsApi.md#updateadkeyword) | **PATCH** /v1/ads/keywords/{keywordId} | Pause or enable a Search keyword |
| [**UpdateAdSet**](AdCampaignsApi.md#updateadset) | **PUT** /v1/ads/ad-sets/{adSetId} | Update an ad set |
| [**UpdateAdSetStatus**](AdCampaignsApi.md#updateadsetstatus) | **PUT** /v1/ads/ad-sets/{adSetId}/status | Pause or resume a single ad set |
| [**UpdateAdStatus**](AdCampaignsApi.md#updateadstatus) | **PUT** /v1/ads/{adId}/status | Pause or resume a single ad |
| [**UpdateBidStrategy**](AdCampaignsApi.md#updatebidstrategy) | **PATCH** /v1/ads/bid-strategies/{strategyId} | Update portfolio bid strategy |
| [**UpdateCampaignAdSchedule**](AdCampaignsApi.md#updatecampaignadschedule) | **PUT** /v1/ads/campaigns/{campaignId}/ad-schedule | Replace a campaign&#39;s ad schedule (dayparting) |
| [**UpdateCampaignAssets**](AdCampaignsApi.md#updatecampaignassets) | **PUT** /v1/ads/campaigns/{campaignId}/assets | Update campaign assets |
| [**UpdateCampaignConversionGoals**](AdCampaignsApi.md#updatecampaignconversiongoals) | **PATCH** /v1/ads/campaigns/{campaignId}/conversion-goals | Update campaign conversion goals |
| [**UpdateCampaignTargeting**](AdCampaignsApi.md#updatecampaigntargeting) | **PUT** /v1/ads/campaigns/{campaignId}/targeting | Edit a Google campaign&#39;s device, location, excluded location, or language targeting |
| [**UpdateGoogleAssetGroup**](AdCampaignsApi.md#updategoogleassetgroup) | **PATCH** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId} | Update a Performance Max asset group |

<a id="addadkeywords"></a>
# **AddAdKeywords**
> AddAdKeywords201Response AddAdKeywords (AddAdKeywordsRequest addAdKeywordsRequest)

Add Search ad-group keywords

Adds one or more keyword criteria to an existing Google Search ad group, without touching the keywords already there (unlike the whole-set diff on `PUT /v1/ads/{adId}`, `keywords`/`negativeKeywords` in `platformSpecificData`, which replaces the set). Set `negative: true` to add ad-group-level negatives instead of positive keywords. 

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
    public class AddAdKeywordsExample
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
            var addAdKeywordsRequest = new AddAdKeywordsRequest(); // AddAdKeywordsRequest | 

            try
            {
                // Add Search ad-group keywords
                AddAdKeywords201Response result = apiInstance.AddAdKeywords(addAdKeywordsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.AddAdKeywords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddAdKeywordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add Search ad-group keywords
    ApiResponse<AddAdKeywords201Response> response = apiInstance.AddAdKeywordsWithHttpInfo(addAdKeywordsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.AddAdKeywordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **addAdKeywordsRequest** | [**AddAdKeywordsRequest**](AddAdKeywordsRequest.md) |  |  |

### Return type

[**AddAdKeywords201Response**](AddAdKeywords201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Keywords added |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="applygooglerecommendations"></a>
# **ApplyGoogleRecommendations**
> ApplyGoogleRecommendations200Response ApplyGoogleRecommendations (ApplyGoogleRecommendationsRequest applyGoogleRecommendationsRequest)

Apply Google Ads recommendations

Apply up to 100 recommendations. This changes the account (budgets, bidding, keywords, assets) and is not reversible or idempotent; Google offers no validate-only mode for it. Items run in partial-failure mode, so one stale recommendation does not block the rest. `parameters` is optional and takes exactly one key named for the recommendation type, in Google's ApplyRecommendationOperation shape (for example `campaignBudget: { newBudgetAmountMicros }` or `keyword: { matchType, cpcBidMicros }`); omit it to apply Google's suggested values.

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
    public class ApplyGoogleRecommendationsExample
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
            var applyGoogleRecommendationsRequest = new ApplyGoogleRecommendationsRequest(); // ApplyGoogleRecommendationsRequest | 

            try
            {
                // Apply Google Ads recommendations
                ApplyGoogleRecommendations200Response result = apiInstance.ApplyGoogleRecommendations(applyGoogleRecommendationsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ApplyGoogleRecommendations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApplyGoogleRecommendationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Apply Google Ads recommendations
    ApiResponse<ApplyGoogleRecommendations200Response> response = apiInstance.ApplyGoogleRecommendationsWithHttpInfo(applyGoogleRecommendationsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ApplyGoogleRecommendationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **applyGoogleRecommendationsRequest** | [**ApplyGoogleRecommendationsRequest**](ApplyGoogleRecommendationsRequest.md) |  |  |

### Return type

[**ApplyGoogleRecommendations200Response**](ApplyGoogleRecommendations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-recommendation outcome. A failed item does not stop the others. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | No Google Ads customer on this connection, or it needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | accountId is not a Google Ads connection. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="attachadgroupassets"></a>
# **AttachAdGroupAssets**
> AttachAdGroupAssets201Response AttachAdGroupAssets (string adSetId, AttachCampaignAssetsRequest attachCampaignAssetsRequest)

Attach ad-group assets

Creates and attaches sitelinks, callouts, structured snippets and image assets in one Google mutation. Google shows images only on accounts it deems eligible (account age, policy history, vertical).

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
    public class AttachAdGroupAssetsExample
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
            var adSetId = "adSetId_example";  // string | Numeric Google platform id.
            var attachCampaignAssetsRequest = new AttachCampaignAssetsRequest(); // AttachCampaignAssetsRequest | 

            try
            {
                // Attach ad-group assets
                AttachAdGroupAssets201Response result = apiInstance.AttachAdGroupAssets(adSetId, attachCampaignAssetsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.AttachAdGroupAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AttachAdGroupAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Attach ad-group assets
    ApiResponse<AttachAdGroupAssets201Response> response = apiInstance.AttachAdGroupAssetsWithHttpInfo(adSetId, attachCampaignAssetsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.AttachAdGroupAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Numeric Google platform id. |  |
| **attachCampaignAssetsRequest** | [**AttachCampaignAssetsRequest**](AttachCampaignAssetsRequest.md) |  |  |

### Return type

[**AttachAdGroupAssets201Response**](AttachAdGroupAssets201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Assets created and attached. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="attachcampaignassets"></a>
# **AttachCampaignAssets**
> AttachCampaignAssets201Response AttachCampaignAssets (string campaignId, AttachCampaignAssetsRequest attachCampaignAssetsRequest)

Attach campaign assets

Creates and attaches sitelinks, callouts, structured snippets and image assets in one Google mutation. Google shows images only on accounts it deems eligible (account age, policy history, vertical).

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
            var campaignId = "campaignId_example";  // string | Numeric Google platform id.
            var attachCampaignAssetsRequest = new AttachCampaignAssetsRequest(); // AttachCampaignAssetsRequest | 

            try
            {
                // Attach campaign assets
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
    // Attach campaign assets
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
| **campaignId** | **string** | Numeric Google platform id. |  |
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
| **201** | Assets created and attached. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="boostpost"></a>
# **BoostPost**
> UpdateAd200Response BoostPost (BoostPostRequest boostPostRequest, string? idempotencyKey = null)

Boost post as ad

Creates a paid ad from an existing published post, keeping the post's engagement. By default it provisions the whole hierarchy (campaign, ad set, ad).  **Attach shape (Meta).** Send `adSetId` to put the ad under an EXISTING ad set instead, so that ad set keeps its learning phase. It then owns `budget`, `schedule` and `targeting`, and sending any of those alongside `adSetId` is a 400 rather than a silent drop. `budget` is required only without `adSetId`.  `instagramAccountId`, `destinationType`, `whatsappPhoneNumber` and `adSetId` are Meta-only and return 400 on other platforms.  `accountId` may be a Facebook, Instagram or Meta ads (business login) connection. A business-login connection has no posting account, so pass the post as `platformPostId` (Facebook `pageId_postId` or an Instagram media id); a Zernio `postId` is a 400 there.  **Messaging boosts (Meta).** Use `goal: engagement` with `callToAction: WHATSAPP_MESSAGE`, `MESSAGE_PAGE`, or `INSTAGRAM_MESSAGE`. The CTA implies WHATSAPP, MESSENGER, or INSTAGRAM_DIRECT respectively; `destinationType` alone does not select a messaging CTA. Omit `linkUrl` only for messaging CTAs. Plain link CTAs keep their goal and link behavior when combined with an independent `destinationType`. The campaign uses OUTCOME_ENGAGEMENT and the ad set uses CONVERSATIONS with the promoted Page. Optional `whatsappPhoneNumber` selects a number already paired with that Page. Conflicting CTA/destination, instant form, goal, or optimizationGoal inputs return 400. Attach requires the target ad set destination to match. Existing post references preserve social proof; an Instagram reel rejected by Meta is not re-uploaded as a new post for a messaging boost.  **Retries.** Boosts are NOT idempotent and can take minutes when Meta requires re-hosting an Instagram video, so do not retry on client timeout. Send an Idempotency-Key header to make retries safe: same key and body replays the original 201, and distinct keys always create distinct ads. Without the header, an identical request is treated as a retry: while one is in flight it returns 409, and within 10 minutes of a completed boost it returns the already-created ad instead of creating another. To intentionally duplicate an ad, send distinct Idempotency-Keys (or vary the body, e.g. the name). 

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. Also returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. An identical boost request is already in progress (with or without an Idempotency-Key). Wait for it to finish instead of retrying.  |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads), missing linked account, or (for TikTok) the connected TikTok user is not authorized as an Identity on the target advertiser. Returned with code &#x60;ads_connection_required&#x60;; the message includes the actionable \&quot;TikTok Ads Manager → Assets → Identity\&quot; remediation step. Also returned as &#x60;idempotency_key_reused&#x60; when an Idempotency-Key is reused with a different request body, and as &#x60;ad_account_unusable&#x60; when Meta refuses writes on the ad account because its status is ineligible to manage ads (see &#x60;ErrorResponse.details&#x60;).  |  -  |
| **429** | Meta only (code &#x60;rate_limited&#x60;). Meta places a security hold lasting days (code 31, subcode 3858385, \&quot;Please authenticate your account\&quot;) on ad accounts that receive bursts of ad writes, and it counts &#x60;validateOnly&#x60; checks as writes. To keep integrations out of that hold, Zernio runs creates for one Meta ad account one at a time (a parallel request waits up to 60 seconds for its turn) and allows at most 30 creates per ad account in any rolling 5 minutes, &#x60;validateOnly&#x60; included. A 429 here means one of the two was hit: wait &#x60;Retry-After&#x60; seconds and send creates for that ad account sequentially. Other ad accounts are not affected.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bulkupdateadcampaignstatus"></a>
# **BulkUpdateAdCampaignStatus**
> BulkUpdateAdCampaignStatus200Response BulkUpdateAdCampaignStatus (BulkUpdateAdCampaignStatusRequest bulkUpdateAdCampaignStatusRequest)

Pause or resume many campaigns

Process up to 50 campaigns in one call. Each campaign is updated concurrently and the response contains a per-campaign result so a single bad row does not fail the whole batch. Each campaign is read, written and re-read exactly as PUT /v1/ads/campaigns/{campaignId}/status describes: only the campaign's own switch is written, never its ad sets' or ads'. `updated` / `skipped` count campaigns. 

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadcampaign"></a>
# **CreateAdCampaign**
> CreateAdCampaign200Response CreateAdCampaign (CreateAdCampaignRequest createAdCampaignRequest, string? idempotencyKey = null)

Create a standalone campaign

Creates a campaign WITHOUT its first ad set / ad, on the platform of the given `accountId`. Ad sets join it later via `existingCampaignId` on the create endpoints. Platform notes: on Meta a budget here is campaign-level (CBO) by definition; omit it for ABO (each ad set carries its own budget), and `specialAdCategories` is Meta-only (400 elsewhere); `bidStrategy` is Meta and Google (400 elsewhere), and Google also accepts `portfolioBidStrategyId` instead. Google, X and OpenAI require a budget (422 without one; OpenAI accepts daily or lifetime, Google only `budgetType: daily`). On OpenAI `goal` sets the campaign objective, and `conversions` needs an active standard conversion event on the account. LinkedIn creates the campaign GROUP (our campaign level) and rejects a budget, which lives on the campaign (ad set) level there; it comes back `status: DRAFT`. Created `PAUSED` (TikTok `DISABLE`) unless `status: ACTIVE` where the platform supports it.  **Idempotency:** send an `Idempotency-Key` header to make retries safe.

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
                CreateAdCampaign200Response result = apiInstance.CreateAdCampaign(createAdCampaignRequest, idempotencyKey);
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
    ApiResponse<CreateAdCampaign200Response> response = apiInstance.CreateAdCampaignWithHttpInfo(createAdCampaignRequest, idempotencyKey);
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

[**CreateAdCampaign200Response**](CreateAdCampaign200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign validation passed without creating a campaign. |  -  |
| **201** | Campaign created |  -  |
| **400** | Invalid input, or Meta rejected the create |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | &#x60;validateOnly: true&#x60; outside Meta, or campaign-only creation on a platform that does not support it. Carries code &#x60;feature_not_available&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadset"></a>
# **CreateAdSet**
> CreateAdSet201Response CreateAdSet (CreateAdSetRequest createAdSetRequest, string? idempotencyKey = null)

Create a standalone ad group

Google Ads compliance row C.190: creates an ad group WITHOUT an ad, under an existing campaign. Ads join it later via `adSetId` on POST /v1/ads/create. Google only; every other platform returns 501.  Created `PAUSED` unless `status: ACTIVE`. The new ad group has no ad yet, so it will not appear in GET /v1/ads/tree (built purely from `ads` rows) until one is added; use GET /v1/ads/ad-sets to see it in the meantime.  **Idempotency:** send an `Idempotency-Key` header to make retries safe.

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
    public class CreateAdSetExample
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
            var createAdSetRequest = new CreateAdSetRequest(); // CreateAdSetRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. (optional) 

            try
            {
                // Create a standalone ad group
                CreateAdSet201Response result = apiInstance.CreateAdSet(createAdSetRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.CreateAdSet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdSetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a standalone ad group
    ApiResponse<CreateAdSet201Response> response = apiInstance.CreateAdSetWithHttpInfo(createAdSetRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.CreateAdSetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createAdSetRequest** | [**CreateAdSetRequest**](CreateAdSetRequest.md) |  |  |
| **idempotencyKey** | **string?** | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. | [optional]  |

### Return type

[**CreateAdSet201Response**](CreateAdSet201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Ad group created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only supported on Google Ads |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createbidstrategy"></a>
# **CreateBidStrategy**
> CreateBidStrategy201Response CreateBidStrategy (CreateBidStrategyRequest createBidStrategyRequest)

Create portfolio bid strategy

Creates a standalone bid strategy shared across campaigns. Attach it to a campaign with `portfolioBidStrategyId` on POST /v1/ads/create, PUT /v1/ads/campaigns/{campaignId}, or PUT /v1/ads/ad-sets/{adSetId}. Attaching a strategy aligned to a shared budget fails there with a 400 (Google's `BIDDING_STRATEGY_AND_BUDGET_MUST_BE_ALIGNED`); this is not retryable.

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
    public class CreateBidStrategyExample
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
            var createBidStrategyRequest = new CreateBidStrategyRequest(); // CreateBidStrategyRequest | 

            try
            {
                // Create portfolio bid strategy
                CreateBidStrategy201Response result = apiInstance.CreateBidStrategy(createBidStrategyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.CreateBidStrategy: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBidStrategyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create portfolio bid strategy
    ApiResponse<CreateBidStrategy201Response> response = apiInstance.CreateBidStrategyWithHttpInfo(createBidStrategyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.CreateBidStrategyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createBidStrategyRequest** | [**CreateBidStrategyRequest**](CreateBidStrategyRequest.md) |  |  |

### Return type

[**CreateBidStrategy201Response**](CreateBidStrategy201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Bid strategy created |  -  |
| **400** | Invalid input, or Google rejected the strategy (e.g. shared-budget alignment). The message carries Google&#39;s error. |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | No Google Ads customer accounts on this connection. Reconnect Google Ads. |  -  |
| **429** | Google Ads operations budget exhausted; retry later. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="creategoogleassetgroup"></a>
# **CreateGoogleAssetGroup**
> CreateGoogleAssetGroup200Response CreateGoogleAssetGroup (string campaignId, CreateGoogleAssetGroupRequest createGoogleAssetGroupRequest)

Create a Performance Max asset group

Add an asset group to an existing Performance Max campaign. The group, any new assets, their links and an optional listing-group tree are created in one atomic request, so Google checks the asset minimums (for non-retail campaigns) against the whole set. Created PAUSED unless status is ENABLED. validateOnly: true runs Google's validation without creating anything.

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
    public class CreateGoogleAssetGroupExample
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
            var campaignId = "campaignId_example";  // string | Google Ads campaign id.
            var createGoogleAssetGroupRequest = new CreateGoogleAssetGroupRequest(); // CreateGoogleAssetGroupRequest | 

            try
            {
                // Create a Performance Max asset group
                CreateGoogleAssetGroup200Response result = apiInstance.CreateGoogleAssetGroup(campaignId, createGoogleAssetGroupRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.CreateGoogleAssetGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateGoogleAssetGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a Performance Max asset group
    ApiResponse<CreateGoogleAssetGroup200Response> response = apiInstance.CreateGoogleAssetGroupWithHttpInfo(campaignId, createGoogleAssetGroupRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.CreateGoogleAssetGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google Ads campaign id. |  |
| **createGoogleAssetGroupRequest** | [**CreateGoogleAssetGroupRequest**](CreateGoogleAssetGroupRequest.md) |  |  |

### Return type

[**CreateGoogleAssetGroup200Response**](CreateGoogleAssetGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | validateOnly request accepted by Google. Nothing was created. |  -  |
| **201** | Asset group created. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | Google Ads connection needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | Campaign is not on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createsharedbudget"></a>
# **CreateSharedBudget**
> CreateSharedBudget201Response CreateSharedBudget (CreateSharedBudgetRequest createSharedBudgetRequest)

Create a shared budget

Creates a daily shared campaign budget (`explicitly_shared: true`, standard delivery) that several campaigns can draw from. A lifetime budget returns 422, like every Google budget. Google refuses some bidding strategies on a shared budget; that error surfaces when a campaign is moved onto it. 

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
    public class CreateSharedBudgetExample
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
            var createSharedBudgetRequest = new CreateSharedBudgetRequest(); // CreateSharedBudgetRequest | 

            try
            {
                // Create a shared budget
                CreateSharedBudget201Response result = apiInstance.CreateSharedBudget(createSharedBudgetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.CreateSharedBudget: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSharedBudgetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a shared budget
    ApiResponse<CreateSharedBudget201Response> response = apiInstance.CreateSharedBudgetWithHttpInfo(createSharedBudgetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.CreateSharedBudgetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createSharedBudgetRequest** | [**CreateSharedBudgetRequest**](CreateSharedBudgetRequest.md) |  |  |

### Return type

[**CreateSharedBudget201Response**](CreateSharedBudget201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Shared budget created |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Lifetime budget requested. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createstandalonead"></a>
# **CreateStandaloneAd**
> CreateStandaloneAd200Response CreateStandaloneAd (CreateStandaloneAdRequest createStandaloneAdRequest, string? idempotencyKey = null)

Create standalone ad

Create a paid ad with custom creative across Meta, Google Ads, Pinterest, TikTok, X, LinkedIn, and OpenAI Ads (ChatGPT Ads).  Google Performance Max: set `campaignType: \"pmax\"` and supply `assetGroup` with text, images by role, business name and finalUrl. Creates a daily budget, PAUSED campaign and asset group atomically. `validateOnly: true` validates the complete request with Google without creating or persisting resources. Read assets with `GET /v1/ads/campaigns/{campaignId}/asset-groups`. The logo is required; video is optional via `assetGroup.youtubeVideoId`. Brand guidelines are disabled at creation. All supplied asset links are validated together against Google's minimum asset requirements. PMax rejects ACTIVE creation, portfolio bidding, bid caps, legacy creative fields and attach shapes. Geo and language targeting are supported; omitted geo targets all locations. PMax does not require top-level goal, headline, body or linkUrl. Supported bidding: omitted or LOWEST_COST_WITHOUT_CAP for Maximize Conversions, COST_CAP plus bidAmount for target CPA, LOWEST_COST_WITH_MIN_ROAS plus roasAverageFloor for Maximize Conversion Value with target ROAS.  Google Demand Gen: set `campaignType: \"demand_gen\"` and supply `demandGen`. Creates a daily budget, PAUSED campaign, one ad group and one ad in a single atomic request: a multi-asset image ad, a video responsive ad when `demandGen.youtubeVideoIds` is sent, or a carousel ad (2 to 10 cards) when `demandGen.carouselCards` is sent. Geo (countries, regions, cities, zips, metros) and languages go on the ad group, as Demand Gen requires. `demandGen.channels` sets the ad group's channel controls and `demandGen.audience` builds a Google Audience (user lists, interests, custom audiences, age ranges, genders) attached to the ad group, or `demandGen.audienceId` attaches an existing one. `validateOnly: true` validates everything with Google without creating resources. Supported bidding: omitted or LOWEST_COST_WITHOUT_CAP for Maximize Conversions, COST_CAP plus bidAmount for target CPA, LOWEST_COST_WITH_MIN_ROAS plus roasAverageFloor for target ROAS, LOWEST_COST_WITH_BID_CAP plus bidAmount for target CPC. The created ad carries the native `platformCampaignId`, `platformAdSetId` (ad group) and `platformAdId`. Activate with PUT /v1/ads/campaigns/{campaignId}/status; budget, bidding and name are edited with the regular campaign endpoints; creative, channels, audience and ad group targeting with PUT /v1/ads/{adId} (`demandGen`, `targeting`). To grow an existing Demand Gen campaign, send `existingCampaignId` (adds a PAUSED ad group, with its own geo, languages, channels and audience, plus its ad) or `adSetId` (adds a PAUSED ad to that ad group); neither takes budget, bidding or schedule fields, and both support `validateOnly`.  Other mutually-exclusive request shapes are selected by the body:  - Legacy single-creative shape (all platforms, the default). - Meta-only multi-creative shape via the creatives array: one ad set with N ads sharing budget and targeting. - Attach shape via adSetId: adds one new ad to an existing ad set, inheriting its budget, targeting, and schedule (Meta, Google Ads, TikTok, and LinkedIn). On LinkedIn adSetId is the existing Campaign id, and the budget, schedule, targeting and bidding fields must be omitted. On LinkedIn `goal` may be omitted too (taken from the Campaign's objective), and the created ad's `targeting` echoes the Campaign's audience.  Meta accepts `creativeFeatures` on the single and attach shapes and as defaults for `creatives[]`; an item replaces the whole feature map. `promotion` is not supported on any shape and any object is rejected with 400. Reusing `existingCreativeId` uses the existing creative settings instead of new settings. Requested settings are persisted for lists, exports, and default ad-detail reads.  Per-platform required fields, budget minimums, and video-ad rules are documented on each property below.  LinkedIn creates a Single Image or Single Video Ad backed by a Direct Sponsored Content \"dark post\" authored by a Company Page (see `organizationId`). Supported goals are engagement, traffic, awareness, and video_views (video ads use the `video` field; video_views requires a video), and traffic ads require `linkUrl`.  **Idempotency:** this endpoint is not idempotent at the platform level (a blind retry creates a second campaign/ad set/ad). Send an `Idempotency-Key` header to make retries safe: the first request with a given key creates the ad and we store the response; a retry with the same key replays that exact response (with `Idempotent-Replayed: true`) instead of creating duplicates. Reusing a key with a different body returns 422; a key whose first request is still in flight returns 409 (retry after a short backoff). Keys are scoped to your credential and expire after 24h. 

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
| **200** | validateOnly dry-run passed, nothing was created |  -  |
| **201** | Ad(s) created |  -  |
| **400** | Missing required fields, invalid values, non-Meta platform used with creatives[] / adSetId, or a Meta validateOnly validation failure (verbatim) |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. Also returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Platform ads connection required (TikTok Ads, X Ads) or missing linked account. Also returned with code &#x60;ad_account_unusable&#x60; when Meta refuses writes on the ad account because its status is ineligible to manage ads (see &#x60;ErrorResponse.details&#x60;).  |  -  |
| **429** | Meta only (code &#x60;rate_limited&#x60;). Meta places a security hold lasting days (code 31, subcode 3858385, \&quot;Please authenticate your account\&quot;) on ad accounts that receive bursts of ad writes, and it counts &#x60;validateOnly&#x60; checks as writes. To keep integrations out of that hold, Zernio runs creates for one Meta ad account one at a time (a parallel request waits up to 60 seconds for its turn) and allows at most 30 creates per ad account in any rolling 5 minutes, &#x60;validateOnly&#x60; included. A 429 here means one of the two was hit: wait &#x60;Retry-After&#x60; seconds and send creates for that ad account sequentially. Other ad accounts are not affected.  |  * Retry-After - Seconds remaining until the upstream quota resets. <br>  |
| **501** | The requested option is not supported on this platform: &#x60;validateOnly&#x60; outside Meta and Google Performance Max, or a shape the adapter does not implement. Carries code &#x60;feature_not_available&#x60;.  |  -  |
| **502** | The platform rejected the request, or failed to produce media the ad needs (e.g. Meta generated no poster for an uploaded video when no &#x60;video.thumbnailUrl&#x60; was supplied). Inspect &#x60;platformError&#x60; for the upstream payload. Failures we raise carry a &#x60;reason&#x60;; a payload forwarded verbatim from Meta may not. On the &#x60;creatives[]&#x60; shape a missing poster also carries &#x60;creativeIndex&#x60; and &#x60;videoUrl&#x60; to identify the entry. An upstream 4xx status is forwarded instead of 502. On Meta, &#x60;details&#x60; names the failing &#x60;stage&#x60;, the &#x60;adAccountId&#x60; and every created object with its cleanup result (see &#x60;ErrorResponse.details&#x60;); an &#x60;unconfirmedWrite&#x60; there means Meta did not confirm a create and Zernio did not retry it.  |  -  |
| **503** | An upstream service or database is temporarily unavailable. Retry after the indicated delay. A timed-out write may have completed upstream; check its outcome before resubmitting. |  * Retry-After - Minimum delay in seconds before retrying. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletead"></a>
# **DeleteAd**
> DeleteAccountGroup200Response DeleteAd (string adId)

Cancel an ad

Deletes the ad on the platform and marks it as cancelled in the database. The ad is preserved for history. OpenAI Ads has no delete API; the ad is archived instead (a terminal state, the closest equivalent).  Only the ad is deleted; a campaign or ad set is never deleted while it still holds another ad. On Meta, when the ad set and campaign were created by Zernio (by `POST /v1/ads/create` or `POST /v1/ads/boost`) and Meta lists no other ad in the ad set (archived ads count), the emptied ad set is deleted too, then the campaign once it holds no other ad set. Parents created outside Zernio, and the parents of an ad imported from the platform, are always kept. On LinkedIn the ad is a creative inside a campaign inside a campaign group: the creative is always removed, the campaign only when Zernio created it and LinkedIn lists no other creative in it that is not archived, canceled or deleted, and the campaign group only when Zernio created it and LinkedIn lists no other campaign in it that is not canceled or deleted (archived campaigns count). If the creative itself cannot be removed the request fails and no parent is touched. To delete a whole campaign on purpose use `DELETE /v1/ads/campaigns/{campaignId}`. 

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
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
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Ad set not found |  -  |
| **501** | Operation not supported on this platform |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="dismissgooglerecommendations"></a>
# **DismissGoogleRecommendations**
> ApplyGoogleRecommendations200Response DismissGoogleRecommendations (DismissGoogleRecommendationsRequest dismissGoogleRecommendationsRequest)

Dismiss Google Ads recommendations

Dismiss up to 100 recommendations so Google stops suggesting them. Items run in partial-failure mode.

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
    public class DismissGoogleRecommendationsExample
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
            var dismissGoogleRecommendationsRequest = new DismissGoogleRecommendationsRequest(); // DismissGoogleRecommendationsRequest | 

            try
            {
                // Dismiss Google Ads recommendations
                ApplyGoogleRecommendations200Response result = apiInstance.DismissGoogleRecommendations(dismissGoogleRecommendationsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.DismissGoogleRecommendations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DismissGoogleRecommendationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Dismiss Google Ads recommendations
    ApiResponse<ApplyGoogleRecommendations200Response> response = apiInstance.DismissGoogleRecommendationsWithHttpInfo(dismissGoogleRecommendationsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.DismissGoogleRecommendationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dismissGoogleRecommendationsRequest** | [**DismissGoogleRecommendationsRequest**](DismissGoogleRecommendationsRequest.md) |  |  |

### Return type

[**ApplyGoogleRecommendations200Response**](ApplyGoogleRecommendations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Per-recommendation outcome. A failed item does not stop the others. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | No Google Ads customer on this connection, or it needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | accountId is not a Google Ads connection. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicatead"></a>
# **DuplicateAd**
> DuplicateAd200Response DuplicateAd (string adId, string? idempotencyKey = null, DuplicateAdRequest? duplicateAdRequest = null)

Duplicate an ad

Duplicates a single ad via Meta's native `POST /{ad-id}/copies`. The copy is created paused. `adSetId` retargets the copy into another ad set; omitted = the source's own ad set. Accepts the Zernio ad id or the platform ad id. Sync discovery is triggered automatically (`syncAfter: false` to skip). Creative settings returned by Meta, including explicit promotion metadata and creativeFeatures, are preserved when the native copy requires a creative rebuild. Metadata Meta does not return cannot be recovered. When Meta refuses the native copy with its capability error (code 3), which happens for some creatives built by other tools, the ad is rebuilt instead: a new creative from the source's returned spec and a new ad in the target ad set, carrying the source name, status option, rename options and tracking specs.

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Ad not found |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicateadcampaign"></a>
# **DuplicateAdCampaign**
> DuplicateAdCampaign200Response DuplicateAdCampaign (string campaignId, DuplicateAdCampaignRequest duplicateAdCampaignRequest, string? idempotencyKey = null)

Duplicate a campaign

Duplicates a campaign, including its ad sets, ads, creatives, and targeting by default (`deepCopy: true`). The copy is created paused so callers can review before launching.  Per-platform implementation: - **Meta** uses the native `POST /{campaign-id}/copies` endpoint. - **TikTok** has no native copy primitive; Zernio walks the source   graph (`/v2/campaign/get/`, `/v2/adgroup/get/`, `/v2/ad/get/`) and   recreates each entity via the corresponding `/create/` endpoints,   carrying over budget / targeting / bid_type / bid_price /   deep_bid_type / creative fields. Spark Ad linkage (`tiktok_item_id`)   is preserved. - **LinkedIn** has no native copy primitive; Zernio walks the source   CampaignGroup → Campaigns → Creatives and recreates each entity,   carrying over `type` / `costType` / `unitCost` /   `optimizationTargetType` / `creativeSelection` / `objectiveType` /   `format` / `dailyBudget` / `totalBudget` / `targetingCriteria` /   `runSchedule` and every Creative's `content` object verbatim.   `statusOption: INHERITED_FROM_SOURCE` is evaluated **per entity**:   any Group / Campaign / Creative whose source is `ACTIVE` gets its   clone activated too. Duplicating an ACTIVE campaign with   `INHERITED_FROM_SOURCE` starts a second front of spend the moment   the clone activates. The safe default is `PAUSED`.  The new hierarchy is asynchronous to materialize in our DB, and we trigger sync discovery automatically. Set `syncAfter: false` to skip and poll `/v1/ads/tree` on your own cadence.  Other platforms return 501 Not Implemented. 

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Source campaign not found |  -  |
| **501** | Operation not supported on this platform |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicateadset"></a>
# **DuplicateAdSet**
> DuplicateAdSet200Response DuplicateAdSet (string adSetId, DuplicateAdSetRequest duplicateAdSetRequest, string? idempotencyKey = null)

Duplicate an ad set

Duplicates an ad set. The copy is created paused so callers can review before launching. `campaignId` retargets the copy into another campaign; omitted = the source's own campaign.  Meta: ads and creatives are included by default (`deepCopy: true`) via Meta's native `POST /{adset-id}/copies`; the new hierarchy materializes asynchronously and sync discovery is triggered automatically (`syncAfter: false` to skip).  TikTok: the ad group is read and recreated under the campaign with its targeting, bidding, budget and schedule (start reset to now); `deepCopy: true` recreates its ads too (default false). `startTime`, `endTime` and `renameStrategy` are ignored and `statusOption` must be PAUSED or absent. The copy appears on the next discovery sync.

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Source ad set not found |  -  |
| **501** | Only supported on Meta (facebook/instagram) and TikTok |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="editgoogleassetgroupassets"></a>
# **EditGoogleAssetGroupAssets**
> EditGoogleAssetGroupAssets200Response EditGoogleAssetGroupAssets (string campaignId, string assetGroupId, EditGoogleAssetGroupAssetsRequest editGoogleAssetGroupAssetsRequest)

Link or unlink asset group assets

Link existing assets or new content to the asset group, and unlink assets, in one atomic request. Links are applied before unlinks, so swapping the last asset of a role does not trip Google's per-role minimum. Unlinking removes the link only; the asset stays in the account library. validateOnly: true validates without writing.

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
    public class EditGoogleAssetGroupAssetsExample
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
            var campaignId = "campaignId_example";  // string | Google Ads campaign id.
            var assetGroupId = "assetGroupId_example";  // string | Google asset group id.
            var editGoogleAssetGroupAssetsRequest = new EditGoogleAssetGroupAssetsRequest(); // EditGoogleAssetGroupAssetsRequest | 

            try
            {
                // Link or unlink asset group assets
                EditGoogleAssetGroupAssets200Response result = apiInstance.EditGoogleAssetGroupAssets(campaignId, assetGroupId, editGoogleAssetGroupAssetsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.EditGoogleAssetGroupAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EditGoogleAssetGroupAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Link or unlink asset group assets
    ApiResponse<EditGoogleAssetGroupAssets200Response> response = apiInstance.EditGoogleAssetGroupAssetsWithHttpInfo(campaignId, assetGroupId, editGoogleAssetGroupAssetsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.EditGoogleAssetGroupAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google Ads campaign id. |  |
| **assetGroupId** | **string** | Google asset group id. |  |
| **editGoogleAssetGroupAssetsRequest** | [**EditGoogleAssetGroupAssetsRequest**](EditGoogleAssetGroupAssetsRequest.md) |  |  |

### Return type

[**EditGoogleAssetGroupAssets200Response**](EditGoogleAssetGroupAssets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Links applied (or validated). |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | Google Ads connection needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | Campaign is not on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getad"></a>
# **GetAd**
> GetAd200Response GetAd (string adId, bool? live = null)

Get ad details

Returns an ad with its creative, targeting, status, and performance metrics. Google Search ads include current creative.headlines, creative.descriptions and creative.finalUrls, preserving pinnedField. Top-level cachedAt and stale report cache freshness. Google mutations invalidate this read. RSA enrichment requires a stored advertisingChannelType of SEARCH. Ads with an unknown or other channel return their stored details without a Google read. If RSA enrichment fails, the stored ad is returned with HTTP 200 and without cache metadata.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: - the Zernio internal `_id` (24-char hex) - Meta's numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`) - the creative's `effective_object_story_id` (`{pageId}_{postId}` shape, Facebook side) - the creative's `effective_instagram_media_id` (Instagram side)  Any of the four resolve to the same ad. Caller doesn't need a translation step. `creative.creativeFeatures` holds the stored requested settings, which do not confirm platform application.  **Status freshness.** `status`, `configuredStatus`, `platformStatus`, `platformAdSetStatus` and `platformCampaignStatus` are the values Zernio last stored. Background sync refreshes them, typically within 15 to 60 minutes (Google up to about 3 hours), and ended or long-paused objects may be refreshed less often. Zernio's own status writes re-read the switches they change. A change made in the platform's own ads manager therefore shows up here only after the next sync. Controllers that act on a switch should pass `live=true`, which reads the switches from the platform now, stores them, and returns `statusReadAt` (null when the read failed and the stored values were returned). With `live=true` the ad's own switch (`configuredStatus`), its delivery status (`status`, `platformStatus`) and its ad set and campaign switches (`platformAdSetStatus`, `platformCampaignStatus`) are read live. 

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
            var live = false;  // bool? | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries `statusReadAt`, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with `statusReadAt: null`. See \"Status freshness\" in the operation description. (optional)  (default to false)

            try
            {
                // Get ad details
                GetAd200Response result = apiInstance.GetAd(adId, live);
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
    ApiResponse<GetAd200Response> response = apiInstance.GetAdWithHttpInfo(adId, live);
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
| **live** | **bool?** | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries &#x60;statusReadAt&#x60;, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with &#x60;statusReadAt: null&#x60;. See \&quot;Status freshness\&quot; in the operation description. | [optional] [default to false] |

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
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadcampaigndetails"></a>
# **GetAdCampaignDetails**
> GetAdCampaignDetails200Response GetAdCampaignDetails (string campaignId, string accountId, string? fields = null)

Get live campaign details

Reads one campaign live from Meta, returned verbatim, so a caller that knows a campaign id no longer has to page `GET /v1/ads/campaigns` to find it. The default projection covers name, status, objective, buying type, bid strategy, budgets, spend cap, schedule and `issues_info`. `fields` is a raw-passthrough override; unknown fields return Meta's 400 verbatim. A campaign the resolved connection cannot see comes back as Meta's own 400, not a 404.

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
    public class GetAdCampaignDetailsExample
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
            var campaignId = "campaignId_example";  // string | Meta campaign id (platformCampaignId).
            var accountId = "accountId_example";  // string | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token.
            var fields = id,name,status,daily_budget;  // string? | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers. (optional) 

            try
            {
                // Get live campaign details
                GetAdCampaignDetails200Response result = apiInstance.GetAdCampaignDetails(campaignId, accountId, fields);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetAdCampaignDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdCampaignDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get live campaign details
    ApiResponse<GetAdCampaignDetails200Response> response = apiInstance.GetAdCampaignDetailsWithHttpInfo(campaignId, accountId, fields);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetAdCampaignDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Meta campaign id (platformCampaignId). |  |
| **accountId** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |  |
| **fields** | **string?** | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers. | [optional]  |

### Return type

[**GetAdCampaignDetails200Response**](GetAdCampaignDetails200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The campaign as returned by Meta |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadreview"></a>
# **GetAdReview**
> GetAdReview200Response GetAdReview (string adId)

Read the platform's review verdict for an ad

Reads the ad's review verdict from the platform now: whether it was approved, where it may not deliver, and every rejection reason with TikTok's suggestion and the piece of content it refers to. Read-only, so it works on a paused ad without re-enabling it.  **Google**: reads `ad_group_ad.policy_summary` live. `approvalStatus` and `reviewStatus` are Google's verbatim (`approvalStatus`: APPROVED, APPROVED_LIMITED, AREA_OF_INTEREST_ONLY, DISAPPROVED, UNKNOWN; `reviewStatus`: REVIEW_IN_PROGRESS, REVIEWED, UNDER_APPEAL, ELIGIBLE_MAY_SERVE); `approved` is true for the three approved statuses, false for DISAPPROVED, null otherwise. `policyTopics` carries every policy topic entry with its `type` (PROHIBITED, LIMITED, ...) and Google's `evidences` and `constraints` verbatim; each PROHIBITED topic is also listed in `rejections` (reason = the topic). The `forbidden*` arrays are TikTok-only and always empty on Google.  TikTok uses `/ad/review_info/`; every other platform returns 501. On TikTok, use it alongside the ad's `platformStatus`: TikTok reports `AD_STATUS_AUDIT` while the ad is in review and `AD_STATUS_AD_PRE_ONLINE` once it passed and is about to deliver (both map to `status: pending_review`); `AD_STATUS_AUDIT_DENY` maps to `rejected`.

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
    public class GetAdReviewExample
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
            var adId = "adId_example";  // string | Zernio ad id (24-char hex) or the platform ad id.

            try
            {
                // Read the platform's review verdict for an ad
                GetAdReview200Response result = apiInstance.GetAdReview(adId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetAdReview: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAdReviewWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read the platform's review verdict for an ad
    ApiResponse<GetAdReview200Response> response = apiInstance.GetAdReviewWithHttpInfo(adId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetAdReviewWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** | Zernio ad id (24-char hex) or the platform ad id. |  |

### Return type

[**GetAdReview200Response**](GetAdReview200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The review verdict |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Ad not found, it has no platform ad id yet, or the platform has no review record for it |  -  |
| **501** | Only supported on TikTok and Google |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadsetdetails"></a>
# **GetAdSetDetails**
> GetAdSetDetails200Response GetAdSetDetails (string adSetId, string accountId, string? fields = null)

Get live ad-set details

Reads the ad set live from Meta, returned verbatim. The default projection includes `learning_stage_info` (learning-phase status: LEARNING / SUCCESS / FAIL / WAIVING; Meta omits its `status` key on paused ad sets), delivery settings, budgets, schedule and targeting. `fields` is a raw-passthrough override; unknown fields return Meta's 400 verbatim.

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
            var fields = id,status,ads.limit(100){id,name,status,issues_info};  // string? | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. (optional) 

            try
            {
                // Get live ad-set details
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
    // Get live ad-set details
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
| **fields** | **string?** | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. | [optional]  |

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
| **400** | Invalid input, or Meta rejected the query; the message carries Meta&#39;s error |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only supported on Meta (facebook/instagram) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadtree"></a>
# **GetAdTree**
> AdTreeResponse GetAdTree (int? page = null, int? limit = null, string? source = null, string? platform = null, AdStatus? status = null, string? adAccountId = null, string? pageId = null, string? accountId = null, string? profileId = null, string? campaignId = null, DateTime? updatedSince = null, string? search = null, DateOnly? fromDate = null, DateOnly? toDate = null, bool? hasDelivery = null, decimal? minSpend = null, string? sort = null, int? timeIncrement = null, string? dailyLevel = null)

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
            var source = "zernio";  // string? | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager. Matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default; use the `status` param for that. (optional)  (default to all)
            var platform = "facebook";  // string? |  (optional) 
            var status = new AdStatus?(); // AdStatus? | Filter by derived campaign status (post-aggregation) (optional) 
            var adAccountId = "adAccountId_example";  // string? | One or more platform ad account IDs to scope the tree to (agency profiles connect a whole Business Manager but a team usually cares about a subset). Comma-separate for multiple (`?adAccountId=act_1,act_2,act_3`); single value keeps its old shape. Max 50 accounts per request; the plural aliases `adAccountIds` and `platformAdAccountIds` are rejected with a 400 to stop them from silently returning the unfiltered fleet. (optional) 
            var pageId = "pageId_example";  // string? | Meta only: Facebook Page ID. Prunes the tree to ads whose creative is backed by this Page: campaigns and ad sets with no ad on the Page drop out, and rolled-up metrics cover only the Page's ads. Mirrors the same filter on /v1/ads and /v1/ads/campaigns. (optional) 
            var accountId = "accountId_example";  // string? | Account ID (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var campaignId = "campaignId_example";  // string? | Restrict the tree to one or more campaigns by platform campaign id (the id the platform assigns, e.g. Meta's numeric campaign id). Comma-separate up to 100 ids (`?campaignId=123,456`). Filters the campaign set itself, so it works regardless of account size and pagination. Pass this when you already hold campaign ids (for example from an `ad.status_changed` webhook) instead of paging the whole tree. (optional) 
            var updatedSince = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? | Return only campaigns with a change stored since this time (ISO 8601 with offset, e.g. `2026-09-30T10:00:00Z`): a new ad, or a change to any ad's status, review status, name, budget or creative. Each matching campaign comes back whole (every ad set and ad). Metrics are not a change: to refresh numbers, filter with `hasDelivery=true` and a date range instead. Combines with every other filter (with `hasDelivery`/`minSpend` a campaign must match both). (optional) 
            var search = "search_example";  // string? | Case-insensitive substring match on campaign, ad set and ad names (`_`, `%` and spaces match literally), or an exact platform campaign, ad set or ad id. A campaign whose name matches returns with all its ad sets and ads; a match on an ad set or ad name returns only the matching branch. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of the METRICS date range (YYYY-MM-DD). On its own it affects only the spend/impression numbers overlaid on each node, not which campaigns are returned. Pass `hasDelivery` or `minSpend` to also filter the campaign set to this window. Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 
            var hasDelivery = true;  // bool? | Return only campaigns that delivered between `fromDate` and `toDate`: spend above zero, or impressions served at zero spend. Unlike `status`, which reads a campaign's CURRENT state, this filters on what happened inside the window, so a campaign that spent then and is paused today is still returned. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. (optional) 
            var minSpend = 8.14D;  // decimal? | Return only campaigns whose spend between `fromDate` and `toDate` reaches this amount. Expressed in each campaign's OWN currency (the `currency` field on the campaign node): spend is stored per ad account in its native currency and one response can span several. Implies `hasDelivery`; `minSpend=0` applies no filter. (optional) 
            var sort = "newest";  // string? | Campaign-level sort order. `newest` (default) / `oldest` order by the campaign's newest-ad createdAt. `spend_desc` / `spend_asc` order by aggregated spend in the requested date range; campaigns with no spend land at the end. (optional)  (default to newest)
            var timeIncrement = 1;  // int? | Set to `1` to also return a daily breakdown. Mirrors Meta Insights' `time_increment=1`: each node gains a `daily[]` array of per-day metrics (same fields as the aggregated `metrics`) alongside the range total, so you get per-entity daily trends in ONE call instead of calling the tree once per day. Only `1` (daily) is supported. The daily series covers the same date range and uses the same source data as `metrics`, except `reach` on Meta and TikTok: the range total is the platform's de-duplicated value, so daily reach does not sum to it. See `dailyLevel` to control which levels carry it. (optional) 
            var dailyLevel = "campaign";  // string? | Which tree levels get the `daily[]` series when `timeIncrement=1`. `campaign` (default) attaches it on campaign nodes only: the common per-campaign-trend case, and the smallest payload. `adset` adds it on ad sets too; `ad` adds it on every ad in `ads[]` as well (heaviest: a long range × up to 100 ads per ad set). Scope with `campaignId` to keep `ad`-level responses small. Ignored when `timeIncrement` is unset. (optional)  (default to campaign)

            try
            {
                // Get campaign tree
                AdTreeResponse result = apiInstance.GetAdTree(page, limit, source, platform, status, adAccountId, pageId, accountId, profileId, campaignId, updatedSince, search, fromDate, toDate, hasDelivery, minSpend, sort, timeIncrement, dailyLevel);
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
    ApiResponse<AdTreeResponse> response = apiInstance.GetAdTreeWithHttpInfo(page, limit, source, platform, status, adAccountId, pageId, accountId, profileId, campaignId, updatedSince, search, fromDate, toDate, hasDelivery, minSpend, sort, timeIncrement, dailyLevel);
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
| **source** | **string?** | &#x60;all&#x60; (default) returns both Zernio-created ads and those discovered from the platform&#39;s ad manager. Matches the web UI&#39;s default view. Pass &#x60;zernio&#x60; to restrict to isExternal&#x3D;false only. Status is NOT filtered by default; use the &#x60;status&#x60; param for that. | [optional] [default to all] |
| **platform** | **string?** |  | [optional]  |
| **status** | [**AdStatus?**](AdStatus?.md) | Filter by derived campaign status (post-aggregation) | [optional]  |
| **adAccountId** | **string?** | One or more platform ad account IDs to scope the tree to (agency profiles connect a whole Business Manager but a team usually cares about a subset). Comma-separate for multiple (&#x60;?adAccountId&#x3D;act_1,act_2,act_3&#x60;); single value keeps its old shape. Max 50 accounts per request; the plural aliases &#x60;adAccountIds&#x60; and &#x60;platformAdAccountIds&#x60; are rejected with a 400 to stop them from silently returning the unfiltered fleet. | [optional]  |
| **pageId** | **string?** | Meta only: Facebook Page ID. Prunes the tree to ads whose creative is backed by this Page: campaigns and ad sets with no ad on the Page drop out, and rolled-up metrics cover only the Page&#39;s ads. Mirrors the same filter on /v1/ads and /v1/ads/campaigns. | [optional]  |
| **accountId** | **string?** | Account ID | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **campaignId** | **string?** | Restrict the tree to one or more campaigns by platform campaign id (the id the platform assigns, e.g. Meta&#39;s numeric campaign id). Comma-separate up to 100 ids (&#x60;?campaignId&#x3D;123,456&#x60;). Filters the campaign set itself, so it works regardless of account size and pagination. Pass this when you already hold campaign ids (for example from an &#x60;ad.status_changed&#x60; webhook) instead of paging the whole tree. | [optional]  |
| **updatedSince** | **DateTime?** | Return only campaigns with a change stored since this time (ISO 8601 with offset, e.g. &#x60;2026-09-30T10:00:00Z&#x60;): a new ad, or a change to any ad&#39;s status, review status, name, budget or creative. Each matching campaign comes back whole (every ad set and ad). Metrics are not a change: to refresh numbers, filter with &#x60;hasDelivery&#x3D;true&#x60; and a date range instead. Combines with every other filter (with &#x60;hasDelivery&#x60;/&#x60;minSpend&#x60; a campaign must match both). | [optional]  |
| **search** | **string?** | Case-insensitive substring match on campaign, ad set and ad names (&#x60;_&#x60;, &#x60;%&#x60; and spaces match literally), or an exact platform campaign, ad set or ad id. A campaign whose name matches returns with all its ad sets and ads; a match on an ad set or ad name returns only the matching branch. Filters the campaign set itself, so &#x60;pagination.total&#x60; counts only matching campaigns. | [optional]  |
| **fromDate** | **DateOnly?** | Start of the METRICS date range (YYYY-MM-DD). On its own it affects only the spend/impression numbers overlaid on each node, not which campaigns are returned. Pass &#x60;hasDelivery&#x60; or &#x60;minSpend&#x60; to also filter the campaign set to this window. Defaults to 90 days ago. | [optional]  |
| **toDate** | **DateOnly?** | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. | [optional]  |
| **hasDelivery** | **bool?** | Return only campaigns that delivered between &#x60;fromDate&#x60; and &#x60;toDate&#x60;: spend above zero, or impressions served at zero spend. Unlike &#x60;status&#x60;, which reads a campaign&#39;s CURRENT state, this filters on what happened inside the window, so a campaign that spent then and is paused today is still returned. Filters the campaign set itself, so &#x60;pagination.total&#x60; counts only matching campaigns. | [optional]  |
| **minSpend** | **decimal?** | Return only campaigns whose spend between &#x60;fromDate&#x60; and &#x60;toDate&#x60; reaches this amount. Expressed in each campaign&#39;s OWN currency (the &#x60;currency&#x60; field on the campaign node): spend is stored per ad account in its native currency and one response can span several. Implies &#x60;hasDelivery&#x60;; &#x60;minSpend&#x3D;0&#x60; applies no filter. | [optional]  |
| **sort** | **string?** | Campaign-level sort order. &#x60;newest&#x60; (default) / &#x60;oldest&#x60; order by the campaign&#39;s newest-ad createdAt. &#x60;spend_desc&#x60; / &#x60;spend_asc&#x60; order by aggregated spend in the requested date range; campaigns with no spend land at the end. | [optional] [default to newest] |
| **timeIncrement** | **int?** | Set to &#x60;1&#x60; to also return a daily breakdown. Mirrors Meta Insights&#39; &#x60;time_increment&#x3D;1&#x60;: each node gains a &#x60;daily[]&#x60; array of per-day metrics (same fields as the aggregated &#x60;metrics&#x60;) alongside the range total, so you get per-entity daily trends in ONE call instead of calling the tree once per day. Only &#x60;1&#x60; (daily) is supported. The daily series covers the same date range and uses the same source data as &#x60;metrics&#x60;, except &#x60;reach&#x60; on Meta and TikTok: the range total is the platform&#39;s de-duplicated value, so daily reach does not sum to it. See &#x60;dailyLevel&#x60; to control which levels carry it. | [optional]  |
| **dailyLevel** | **string?** | Which tree levels get the &#x60;daily[]&#x60; series when &#x60;timeIncrement&#x3D;1&#x60;. &#x60;campaign&#x60; (default) attaches it on campaign nodes only: the common per-campaign-trend case, and the smallest payload. &#x60;adset&#x60; adds it on ad sets too; &#x60;ad&#x60; adds it on every ad in &#x60;ads[]&#x60; as well (heaviest: a long range × up to 100 ads per ad set). Scope with &#x60;campaignId&#x60; to keep &#x60;ad&#x60;-level responses small. Ignored when &#x60;timeIncrement&#x60; is unset. | [optional] [default to campaign] |

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getadstimeline"></a>
# **GetAdsTimeline**
> AdsTimelineResponse GetAdsTimeline (string accountId, string? adAccountId = null, DateOnly? fromDate = null, DateOnly? toDate = null, string? platform = null)

Get daily account metrics

Returns daily aggregate metrics across all ads in a SocialAccount as a single time series, one row per calendar day in the requested range. Use this for dashboards that draw a daily-spend or daily-conversions chart, instead of calling `/v1/ads/tree` once per day.  `accountId` is required. The lookup is sibling-expanded so passing the `metaads` ID also includes ads under the linked `facebook` / `instagram` posting account (and vice-versa), the same convention as `/v1/ads/tree` and `/v1/ads`.  Date range defaults to the last 90 days. Capped at 730 days. Ranges older than the ingested history return a `202` immediately with the covered part and `backfillPending: true` while the rest is backfilled in the background; repeat the request shortly until it returns 200 with full data.  With adAccountId set to a Google customer id this is the customer-level performance report (clicks, cost, impressions, conversions, all conversions per day). 

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
            var accountId = "accountId_example";  // string | Account ID. Sibling-expanded to its linked posting↔ads pair.
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
| **accountId** | **string** | Account ID. Sibling-expanded to its linked posting↔ads pair. |  |
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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignadschedule"></a>
# **GetCampaignAdSchedule**
> GetCampaignAdSchedule200Response GetCampaignAdSchedule (string campaignId, string? platform = null, bool? includePerformance = null, int? windowDays = null, DateOnly? fromDate = null, DateOnly? toDate = null)

Read a campaign's ad schedule (dayparting)

The windows a Google campaign serves in, with the bid modifier on each, plus the criterion ids Google minted for them.  An EMPTY `schedule` is meaningful and is not a failed lookup: Google has no \"all day\" criterion, so a campaign with no ad schedule serves around the clock. `servesAroundTheClock` states that explicitly.  Set `includePerformance=true` to also get delivery split by day of week and by hour, which is the evidence for deciding what the schedule should be. It is one extra Google call segmented by both dimensions at once, so the two views always agree.  Google Ads only. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read. 

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
    public class GetCampaignAdScheduleExample
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
            var platform = "google";  // string? | Disambiguates the campaign id when the connection spans platforms. (optional) 
            var includePerformance = true;  // bool? | Also return delivery by day of week and by hour. Costs one extra Google call. (optional) 
            var windowDays = 30;  // int? | Trailing window for the performance split. Ignored when fromDate and toDate are both given. (optional)  (default to 30)
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of an explicit performance range (YYYY-MM-DD). Use together with toDate. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of an explicit performance range (YYYY-MM-DD). Must be on or after fromDate. (optional) 

            try
            {
                // Read a campaign's ad schedule (dayparting)
                GetCampaignAdSchedule200Response result = apiInstance.GetCampaignAdSchedule(campaignId, platform, includePerformance, windowDays, fromDate, toDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetCampaignAdSchedule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignAdScheduleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a campaign's ad schedule (dayparting)
    ApiResponse<GetCampaignAdSchedule200Response> response = apiInstance.GetCampaignAdScheduleWithHttpInfo(campaignId, platform, includePerformance, windowDays, fromDate, toDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetCampaignAdScheduleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Numeric Google platform campaign id. |  |
| **platform** | **string?** | Disambiguates the campaign id when the connection spans platforms. | [optional]  |
| **includePerformance** | **bool?** | Also return delivery by day of week and by hour. Costs one extra Google call. | [optional]  |
| **windowDays** | **int?** | Trailing window for the performance split. Ignored when fromDate and toDate are both given. | [optional] [default to 30] |
| **fromDate** | **DateOnly?** | Start of an explicit performance range (YYYY-MM-DD). Use together with toDate. | [optional]  |
| **toDate** | **DateOnly?** | End of an explicit performance range (YYYY-MM-DD). Must be on or after fromDate. | [optional]  |

### Return type

[**GetCampaignAdSchedule200Response**](GetCampaignAdSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The campaign&#39;s ad schedule |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **501** | Not a Google Ads campaign: ad schedules are a Google criterion. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignbidding"></a>
# **GetCampaignBidding**
> GetCampaignBidding200Response GetCampaignBidding (string campaignId, string accountId, string platform, string? adAccountId = null, string? customerId = null)

Read a campaign's current bidding

Read of the campaign's bidding strategy on Google, cached for the quota window, for pre-filling the bid strategy block before a PUT to /v1/ads/campaigns/{campaignId}. Google Ads only; `platform` is required and rejected when it is anything else, since a `campaignId` is not globally unique. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read.  Maps Google's bidding strategy onto the same triplet PUT accepts: `LOWEST_COST_WITHOUT_CAP` (Maximize Conversions, no target), `COST_CAP` + `bidAmount` (Target CPA), `LOWEST_COST_WITH_MIN_ROAS` + `roasAverageFloor` (Target ROAS), `LOWEST_COST_WITH_BID_CAP` + `bidAmount` (Maximize Clicks with a CPC ceiling). A campaign on a portfolio strategy returns `portfolio` (id + name) and `bidSpec.portfolioBidStrategyId` instead of the triplet. Anything else (Manual CPC, Target Impression Share, ...) returns `bidSpec: null`; show `biddingStrategyType` as-is. 

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
    public class GetCampaignBiddingExample
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
            var accountId = "accountId_example";  // string | Zernio Google Ads SocialAccount id: resolves the customer id + refresh token.
            var platform = "google";  // string | Required: campaign IDs are not globally unique. Only \"google\" is supported today.
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple Google Ads accounts; optional (and inferred) when it has only one. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId, kept for existing callers (optional) 

            try
            {
                // Read a campaign's current bidding
                GetCampaignBidding200Response result = apiInstance.GetCampaignBidding(campaignId, accountId, platform, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetCampaignBidding: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignBiddingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a campaign's current bidding
    ApiResponse<GetCampaignBidding200Response> response = apiInstance.GetCampaignBiddingWithHttpInfo(campaignId, accountId, platform, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetCampaignBiddingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Numeric Google platform campaign id. |  |
| **accountId** | **string** | Zernio Google Ads SocialAccount id: resolves the customer id + refresh token. |  |
| **platform** | **string** | Required: campaign IDs are not globally unique. Only \&quot;google\&quot; is supported today. |  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple Google Ads accounts; optional (and inferred) when it has only one. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId, kept for existing callers | [optional]  |

### Return type

[**GetCampaignBidding200Response**](GetCampaignBidding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign bidding |  -  |
| **400** | Invalid input (accountId, adAccountId, or a non-numeric campaignId), or a platform other than \&quot;google\&quot; |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Not a Google Ads account: the connection behind accountId resolves to another platform. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaignconversiongoals"></a>
# **GetCampaignConversionGoals**
> GetCampaignConversionGoals200Response GetCampaignConversionGoals (string campaignId)

Get campaign conversion goals

A Google campaign's conversion goals (CampaignConversionGoal, `biddable` per category and origin) and its goal config (ConversionGoalCampaignConfig): `goalConfigLevel` CUSTOMER means the campaign follows the account-default goals, CAMPAIGN means it uses its own goals or `customConversionGoalId`.

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
    public class GetCampaignConversionGoalsExample
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
            var campaignId = "campaignId_example";  // string | Google campaign id

            try
            {
                // Get campaign conversion goals
                GetCampaignConversionGoals200Response result = apiInstance.GetCampaignConversionGoals(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetCampaignConversionGoals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignConversionGoalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get campaign conversion goals
    ApiResponse<GetCampaignConversionGoals200Response> response = apiInstance.GetCampaignConversionGoalsWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetCampaignConversionGoalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google campaign id |  |

### Return type

[**GetCampaignConversionGoals200Response**](GetCampaignConversionGoals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign conversion goals |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Campaign not found |  -  |
| **409** | Campaign matches multiple accessible accounts, or the connection needs reconnecting |  -  |
| **501** | Only available on Google Ads campaigns |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcampaigntargeting"></a>
# **GetCampaignTargeting**
> GetCampaignTargeting200Response GetCampaignTargeting (string campaignId, string? platform = null)

Read a Google campaign's device, location, excluded location, and language targeting

Google Ads compliance requires geo, language, budget, and bidding targeting set at creation to stay editable afterwards; this reads the campaign state so an integrator can build an editor around it. Cached for the quota window (10 minutes fresh, up to 7 days last-good), not always a live read. Google only; every other platform returns 501.  `devices` lists the device criteria the campaign carries, which depends on its channel: Search campaigns have MOBILE, DESKTOP and TABLET, Display campaigns also have CONNECTED_TV. `bidModifier` is Google's bid adjustment for that device, `null` when it has none, and `0` when the device is switched off; `included` is false for exactly that case.  `excludedLocations` lists the campaign's negative location criteria (the places it never serves in). `locations` still lists every location criterion, each flagged with `negative`, so a client reading the targeted set filters `negative: false`. 

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
    public class GetCampaignTargetingExample
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
            var campaignId = "campaignId_example";  // string | Google platform campaign ID
            var platform = "google";  // string? | Disambiguates when the same campaignId string exists on more than one connected platform. (optional) 

            try
            {
                // Read a Google campaign's device, location, excluded location, and language targeting
                GetCampaignTargeting200Response result = apiInstance.GetCampaignTargeting(campaignId, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetCampaignTargeting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCampaignTargetingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Read a Google campaign's device, location, excluded location, and language targeting
    ApiResponse<GetCampaignTargeting200Response> response = apiInstance.GetCampaignTargetingWithHttpInfo(campaignId, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetCampaignTargetingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google platform campaign ID |  |
| **platform** | **string?** | Disambiguates when the same campaignId string exists on more than one connected platform. | [optional]  |

### Return type

[**GetCampaignTargeting200Response**](GetCampaignTargeting200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Current campaign targeting |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans). |  -  |
| **404** | Campaign not found |  -  |
| **501** | Only available on Google Ads campaigns |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getgoogleassetgroup"></a>
# **GetGoogleAssetGroup**
> GetGoogleAssetGroup200Response GetGoogleAssetGroup (string campaignId, string assetGroupId)

Get a Performance Max asset group

One asset group with its linked assets, ad strength, primary status and listing-group tree. Uses a 10-minute cache, served stale when Google quota is exhausted; any write below clears it.

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
    public class GetGoogleAssetGroupExample
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
            var campaignId = "campaignId_example";  // string | Google Ads campaign id.
            var assetGroupId = "assetGroupId_example";  // string | Google asset group id.

            try
            {
                // Get a Performance Max asset group
                GetGoogleAssetGroup200Response result = apiInstance.GetGoogleAssetGroup(campaignId, assetGroupId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.GetGoogleAssetGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGoogleAssetGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a Performance Max asset group
    ApiResponse<GetGoogleAssetGroup200Response> response = apiInstance.GetGoogleAssetGroupWithHttpInfo(campaignId, assetGroupId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.GetGoogleAssetGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google Ads campaign id. |  |
| **assetGroupId** | **string** | Google asset group id. |  |

### Return type

[**GetGoogleAssetGroup200Response**](GetGoogleAssetGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The asset group. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | Google Ads connection needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | Campaign is not on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadcampaigns"></a>
# **ListAdCampaigns**
> ListAdCampaigns200Response ListAdCampaigns (bool? includeEmpty = null, int? page = null, int? limit = null, string? source = null, string? platform = null, AdStatus? status = null, string? adAccountId = null, string? campaignId = null, string? pageId = null, string? accountId = null, string? profileId = null, DateOnly? fromDate = null, DateOnly? toDate = null, bool? hasDelivery = null, decimal? minSpend = null, bool? live = null)

List campaigns

Returns campaigns as virtual aggregations over ad documents grouped by platform campaign ID. Metrics (spend, impressions, clicks, etc.) are summed across all ads in each campaign. Campaign status is derived from child ad statuses (active > pending_review > paused > error > completed > cancelled > rejected). Google campaign budgets include amountMicros, explicitlyShared, resourceName and deliveryMethod after the next successful sync. This endpoint does not fetch Google live.  **Status freshness.** `status`, `configuredStatus`, `platformStatus`, `platformAdSetStatus` and `platformCampaignStatus` are the values Zernio last stored. Background sync refreshes them, typically within 15 to 60 minutes (Google up to about 3 hours), and ended or long-paused objects may be refreshed less often. Zernio's own status writes re-read the switches they change. A change made in the platform's own ads manager therefore shows up here only after the next sync. Controllers that act on a switch should pass `live=true`, which reads the switches from the platform now, stores them, and returns `statusReadAt` (null when the read failed and the stored values were returned). With `live=true` (which needs `limit` of 20 or less) each returned campaign's own switch (`platformCampaignStatus`) is read live. Live reads cover TikTok, Meta, Google and OpenAI. The rolled-up `status` is not re-derived by a live read.  **Budgets here are SYNCED**, never read live, including with `live=true`. To read the current budgets (and status) of every campaign and ad set of a Meta ad account live in one call, for example as a pre-write spend gate, use GET /v1/ads/accounts/live. 

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
            var includeEmpty = true;  // bool? | Meta only. Campaign reads aggregate over ad documents, so a campaign with ZERO ads is normally invisible here, the state the two-step create (campaign, then ads via `existingCampaignId`) leaves behind whenever Meta rejects the ad step. Set true to list those too, with `adCount: 0` and zeroed metrics. Requires `accountId` and `adAccountId`, since an empty campaign has no ad row to resolve a token or ad account from. (optional) 
            var page = 1;  // int? | Page number (1-based) (optional)  (default to 1)
            var limit = 20;  // int? |  (optional)  (default to 20)
            var source = "zernio";  // string? | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager. Matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default; use the `status` param for that. (optional)  (default to all)
            var platform = "facebook";  // string? |  (optional) 
            var status = new AdStatus?(); // AdStatus? | Filter by derived campaign status (post-aggregation) (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (e.g. act_123 for Meta) (optional) 
            var campaignId = "campaignId_example";  // string? | Platform campaign ID (the `platformCampaignId` on each returned campaign). Returns only that campaign, or an empty list when it is not visible to the caller. Mirrors the same filter on /v1/ads and /v1/ads/tree. (optional) 
            var pageId = "pageId_example";  // string? | Meta only: Facebook Page ID. Campaigns have no Page of their own, so this keeps campaigns having at least one ad backed by this Page, with adCount and metrics computed over those ads only. Mirrors the same filter on /v1/ads and /v1/ads/tree. (optional) 
            var accountId = "accountId_example";  // string? | Account ID (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of metrics date range (YYYY-MM-DD, inclusive). Defaults to 90 days ago when both date params are omitted. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of metrics date range (YYYY-MM-DD, inclusive). Defaults to today. Max 730-day range. (optional) 
            var hasDelivery = true;  // bool? | Return only campaigns that delivered between `fromDate` and `toDate`: spend above zero, or impressions served at zero spend. Unlike `status`, which reads a campaign's CURRENT state, this filters on what happened inside the window. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. Mirrors the same filter on /v1/ads/tree. (optional) 
            var minSpend = 8.14D;  // decimal? | Return only campaigns whose spend between `fromDate` and `toDate` reaches this amount, in each campaign's OWN currency (the `currency` field on the campaign). Implies `hasDelivery`; `minSpend=0` applies no filter. Mirrors the same filter on /v1/ads/tree. (optional) 
            var live = false;  // bool? | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries `statusReadAt`, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with `statusReadAt: null`. See \"Status freshness\" in the operation description. (optional)  (default to false)

            try
            {
                // List campaigns
                ListAdCampaigns200Response result = apiInstance.ListAdCampaigns(includeEmpty, page, limit, source, platform, status, adAccountId, campaignId, pageId, accountId, profileId, fromDate, toDate, hasDelivery, minSpend, live);
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
    ApiResponse<ListAdCampaigns200Response> response = apiInstance.ListAdCampaignsWithHttpInfo(includeEmpty, page, limit, source, platform, status, adAccountId, campaignId, pageId, accountId, profileId, fromDate, toDate, hasDelivery, minSpend, live);
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
| **includeEmpty** | **bool?** | Meta only. Campaign reads aggregate over ad documents, so a campaign with ZERO ads is normally invisible here, the state the two-step create (campaign, then ads via &#x60;existingCampaignId&#x60;) leaves behind whenever Meta rejects the ad step. Set true to list those too, with &#x60;adCount: 0&#x60; and zeroed metrics. Requires &#x60;accountId&#x60; and &#x60;adAccountId&#x60;, since an empty campaign has no ad row to resolve a token or ad account from. | [optional]  |
| **page** | **int?** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **int?** |  | [optional] [default to 20] |
| **source** | **string?** | &#x60;all&#x60; (default) returns both Zernio-created ads and those discovered from the platform&#39;s ad manager. Matches the web UI&#39;s default view. Pass &#x60;zernio&#x60; to restrict to isExternal&#x3D;false only. Status is NOT filtered by default; use the &#x60;status&#x60; param for that. | [optional] [default to all] |
| **platform** | **string?** |  | [optional]  |
| **status** | [**AdStatus?**](AdStatus?.md) | Filter by derived campaign status (post-aggregation) | [optional]  |
| **adAccountId** | **string?** | Platform ad account ID (e.g. act_123 for Meta) | [optional]  |
| **campaignId** | **string?** | Platform campaign ID (the &#x60;platformCampaignId&#x60; on each returned campaign). Returns only that campaign, or an empty list when it is not visible to the caller. Mirrors the same filter on /v1/ads and /v1/ads/tree. | [optional]  |
| **pageId** | **string?** | Meta only: Facebook Page ID. Campaigns have no Page of their own, so this keeps campaigns having at least one ad backed by this Page, with adCount and metrics computed over those ads only. Mirrors the same filter on /v1/ads and /v1/ads/tree. | [optional]  |
| **accountId** | **string?** | Account ID | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **fromDate** | **DateOnly?** | Start of metrics date range (YYYY-MM-DD, inclusive). Defaults to 90 days ago when both date params are omitted. | [optional]  |
| **toDate** | **DateOnly?** | End of metrics date range (YYYY-MM-DD, inclusive). Defaults to today. Max 730-day range. | [optional]  |
| **hasDelivery** | **bool?** | Return only campaigns that delivered between &#x60;fromDate&#x60; and &#x60;toDate&#x60;: spend above zero, or impressions served at zero spend. Unlike &#x60;status&#x60;, which reads a campaign&#39;s CURRENT state, this filters on what happened inside the window. Filters the campaign set itself, so &#x60;pagination.total&#x60; counts only matching campaigns. Mirrors the same filter on /v1/ads/tree. | [optional]  |
| **minSpend** | **decimal?** | Return only campaigns whose spend between &#x60;fromDate&#x60; and &#x60;toDate&#x60; reaches this amount, in each campaign&#39;s OWN currency (the &#x60;currency&#x60; field on the campaign). Implies &#x60;hasDelivery&#x60;; &#x60;minSpend&#x3D;0&#x60; applies no filter. Mirrors the same filter on /v1/ads/tree. | [optional]  |
| **live** | **bool?** | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries &#x60;statusReadAt&#x60;, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with &#x60;statusReadAt: null&#x60;. See \&quot;Status freshness\&quot; in the operation description. | [optional] [default to false] |

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadgroupassets"></a>
# **ListAdGroupAssets**
> ListAdGroupAssets200Response ListAdGroupAssets (string adSetId, string accountId, string? adAccountId = null, string? customerId = null)

List ad-group assets

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

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
    public class ListAdGroupAssetsExample
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
            var adSetId = "adSetId_example";  // string | Numeric Google platform id.
            var accountId = "accountId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string? |  (optional) 
            var customerId = "customerId_example";  // string? |  (optional) 

            try
            {
                // List ad-group assets
                ListAdGroupAssets200Response result = apiInstance.ListAdGroupAssets(adSetId, accountId, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListAdGroupAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdGroupAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ad-group assets
    ApiResponse<ListAdGroupAssets200Response> response = apiInstance.ListAdGroupAssetsWithHttpInfo(adSetId, accountId, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListAdGroupAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Numeric Google platform id. |  |
| **accountId** | **string** |  |  |
| **adAccountId** | **string?** |  | [optional]  |
| **customerId** | **string?** |  | [optional]  |

### Return type

[**ListAdGroupAssets200Response**](ListAdGroupAssets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadkeywords"></a>
# **ListAdKeywords**
> ListAdKeywords200Response ListAdKeywords (int? page = null, int? limit = null, string? accountId = null, string? adAccountId = null, string? profileId = null, string? campaignId = null, string? adSetId = null, string? status = null, string? matchType = null, bool? negative = null, string? search = null)

List Search keywords

Returns the Google Search keyword criteria (positive and negative) synced from connected Google Ads accounts, one row per ad-group keyword. Refreshed about once a day per Google Ads customer (the keyword sweep rides the ads discovery pass on a slower slot), so keywords added on Google can take up to a day to appear. A customer synced for the first time is populated on the next discovery pass rather than waiting for its daily slot, and connecting an account or triggering a manual sync refreshes it immediately. Campaign-level negative keywords are not included; only ad-group-level criteria are. 

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
            var accountId = "accountId_example";  // string? | Account ID (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID). Mirrors the same filter on /v1/ads. (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var campaignId = "campaignId_example";  // string? | Platform campaign ID (optional) 
            var adSetId = "adSetId_example";  // string? | Platform ad group ID (Google ad group) (optional) 
            var status = "active";  // string? | Keyword criterion status (optional) 
            var matchType = "exact";  // string? | Accepted in any case. (optional) 
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
| **accountId** | **string?** | Account ID | [optional]  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID). Mirrors the same filter on /v1/ads. | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **campaignId** | **string?** | Platform campaign ID | [optional]  |
| **adSetId** | **string?** | Platform ad group ID (Google ad group) | [optional]  |
| **status** | **string?** | Keyword criterion status | [optional]  |
| **matchType** | **string?** | Accepted in any case. | [optional]  |
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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listadsets"></a>
# **ListAdSets**
> ListAdSets200Response ListAdSets (string? accountId = null, string? adAccountId = null, string? campaignId = null, string? adSetId = null, string? platform = null, bool? live = null)

List ad sets

Ad sets (Google ad groups) synced for the connection, optionally filtered by platform and campaignId. Reads the `ad_sets` table directly, independent of the `ads` rollup GET /v1/ads/tree uses, so a newly created standalone ad group with no ad yet (POST /v1/ads/ad-sets, Google only) is visible here even though it is invisible in the tree until an ad joins it via `adSetId` on POST /v1/ads/create. Returns at most 500 rows, newest first.  **This list is SYNCED, not live** (refreshed by background sync, see below). Each row also carries the ad set's config (`targeting`, `bidStrategy`, `bidAmount`, `optimizationGoal`, `billingEvent`, `promotedObject`), so `?accountId=...&adAccountId=act_...` returns the config of every ad set of an ad account in one call, without a `campaignId`. To read budgets, status, targeting, promoted object and bid strategy of every campaign and ad set of a Meta ad account LIVE in one call (for example as a pre-write spend gate), use GET /v1/ads/accounts/live instead.  **Status freshness.** `status`, `configuredStatus`, `platformStatus`, `platformAdSetStatus` and `platformCampaignStatus` are the values Zernio last stored. Background sync refreshes them, typically within 15 to 60 minutes (Google up to about 3 hours), and ended or long-paused objects may be refreshed less often. Zernio's own status writes re-read the switches they change. A change made in the platform's own ads manager therefore shows up here only after the next sync. Controllers that act on a switch should pass `live=true`, which reads the switches from the platform now, stores them, and returns `statusReadAt` (null when the read failed and the stored values were returned). With `live=true` (which needs a `campaignId` or `adSetId` filter) each listed ad set's own switch (`platformAdSetStatus`) is read live, for the first 20 rows; later rows keep their synced value with `statusReadAt: null`. Live reads cover TikTok, Meta, Google and OpenAI. The rolled-up `status` is not re-derived by a live read. On TikTok the same live read also returns the ad group's applied `optimizationGoal` and `billingEvent`, as TikTok's adgroup/get reports them, so you can verify the goal TikTok applied rather than the one you requested. It also returns `nativeSettings`: TikTok's own adgroup/get record for the ad group, verbatim and read in that same call (budget, budget_mode, schedule, placements, locations, ages, gender, languages, interests, actions, audiences and exclusions), plus the advertiser's currency and timezone. TikTok's `schedule_start_time` / `schedule_end_time` are UTC wall clocks (\"YYYY-MM-DD HH:MM:SS\", no offset); Ads Manager displays them in `advertiser_timezone`. `configReadAt` says when it was read; it is null on every row whose native settings were not read now, so never treat a null as a match. These are read, not retained create payloads, and are not stored.

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
    public class ListAdSetsExample
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
            var accountId = "accountId_example";  // string? | Account ID (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account id (Meta act_<n>). Lists every synced ad set of that ad account; no campaignId needed. (optional) 
            var campaignId = "campaignId_example";  // string? | Platform campaign ID (optional) 
            var adSetId = "adSetId_example";  // string? | Platform ad set ID (optional) 
            var platform = "facebook";  // string? |  (optional) 
            var live = false;  // bool? | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries `statusReadAt`, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with `statusReadAt: null`. See \"Status freshness\" in the operation description. (optional)  (default to false)

            try
            {
                // List ad sets
                ListAdSets200Response result = apiInstance.ListAdSets(accountId, adAccountId, campaignId, adSetId, platform, live);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListAdSets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAdSetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ad sets
    ApiResponse<ListAdSets200Response> response = apiInstance.ListAdSetsWithHttpInfo(accountId, adAccountId, campaignId, adSetId, platform, live);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListAdSetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string?** | Account ID | [optional]  |
| **adAccountId** | **string?** | Platform ad account id (Meta act_&lt;n&gt;). Lists every synced ad set of that ad account; no campaignId needed. | [optional]  |
| **campaignId** | **string?** | Platform campaign ID | [optional]  |
| **adSetId** | **string?** | Platform ad set ID | [optional]  |
| **platform** | **string?** |  | [optional]  |
| **live** | **bool?** | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries &#x60;statusReadAt&#x60;, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with &#x60;statusReadAt: null&#x60;. See \&quot;Status freshness\&quot; in the operation description. | [optional] [default to false] |

### Return type

[**ListAdSets200Response**](ListAdSets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ad sets |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required (Ads add-on on legacy plans, included on usage-based plans). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listads"></a>
# **ListAds**
> AdsListResponse ListAds (int? page = null, int? limit = null, string? source = null, AdStatus? status = null, string? platform = null, string? accountId = null, string? adAccountId = null, string? pageId = null, string? profileId = null, string? campaignId = null, string? adSetId = null, string? platformAdId = null, string? effectiveObjectStoryId = null, string? effectiveInstagramMediaId = null, DateOnly? fromDate = null, DateOnly? toDate = null)

List ads

Returns a paginated list of ads with metrics computed over an optional date range. Use source=all to include externally-synced ads from platform ad managers. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max.  To find the Zernio ad behind a comment you see in Meta Business Manager, filter by platformAdId (the Meta ad ID), effectiveObjectStoryId (Facebook), or effectiveInstagramMediaId (Instagram). Those are the post/media the ad's engagement lives on, and are also returned on each ad's `creative` object. Then call GET /v1/ads/{adId}/comments with the returned ad id. 

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
            var accountId = "accountId_example";  // string? | Account ID (optional) 
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. (optional) 
            var pageId = "pageId_example";  // string? | Meta only: Facebook Page ID. Returns only ads whose creative is backed by this Page (a Meta ad account serves ads for every Page in the Business Manager). Matches each ad's `creative.pageId`; ads with no page signal (rare IG-only creatives) never match. Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. (optional) 
            var profileId = "profileId_example";  // string? | Profile ID (optional) 
            var campaignId = "campaignId_example";  // string? | Platform campaign ID (filter ads within a campaign) (optional) 
            var adSetId = "adSetId_example";  // string? | Platform ad set ID (filter ads within an ad set, the /{adset_id}/ads read of an adset-centric dashboard). (optional) 
            var platformAdId = "platformAdId_example";  // string? | Meta ad ID. Returns the ad with this platform-side ad ID. (optional) 
            var effectiveObjectStoryId = "effectiveObjectStoryId_example";  // string? | Facebook `{pageId}_{postId}` of the post the ad's engagement lives on (Meta `effective_object_story_id`). Use to map a Business-Manager-visible post back to the Zernio ad. (optional) 
            var effectiveInstagramMediaId = "effectiveInstagramMediaId_example";  // string? | Instagram media ID of the boosted post (Meta `effective_instagram_media_id`). Use to map a Business-Manager-visible IG post back to the Zernio ad. (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. (optional) 

            try
            {
                // List ads
                AdsListResponse result = apiInstance.ListAds(page, limit, source, status, platform, accountId, adAccountId, pageId, profileId, campaignId, adSetId, platformAdId, effectiveObjectStoryId, effectiveInstagramMediaId, fromDate, toDate);
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
    ApiResponse<AdsListResponse> response = apiInstance.ListAdsWithHttpInfo(page, limit, source, status, platform, accountId, adAccountId, pageId, profileId, campaignId, adSetId, platformAdId, effectiveObjectStoryId, effectiveInstagramMediaId, fromDate, toDate);
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
| **accountId** | **string?** | Account ID | [optional]  |
| **adAccountId** | **string?** | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. | [optional]  |
| **pageId** | **string?** | Meta only: Facebook Page ID. Returns only ads whose creative is backed by this Page (a Meta ad account serves ads for every Page in the Business Manager). Matches each ad&#39;s &#x60;creative.pageId&#x60;; ads with no page signal (rare IG-only creatives) never match. Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. | [optional]  |
| **profileId** | **string?** | Profile ID | [optional]  |
| **campaignId** | **string?** | Platform campaign ID (filter ads within a campaign) | [optional]  |
| **adSetId** | **string?** | Platform ad set ID (filter ads within an ad set, the /{adset_id}/ads read of an adset-centric dashboard). | [optional]  |
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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbidstrategies"></a>
# **ListBidStrategies**
> ListBidStrategies200Response ListBidStrategies (string accountId, string? adAccountId = null, string? customerId = null, DateOnly? fromDate = null, DateOnly? toDate = null)

List portfolio bid strategies

Bidding strategy report: type, status, campaign count, clicks, cost, cost per conversion, impressions, average CPC and conversions over the date range (default last 30 days). Reads Google's `bidding_strategy` resource, cached for the quota window. Draws on the shared Google Ads operations budget. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read.

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
    public class ListBidStrategiesExample
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
            var accountId = "accountId_example";  // string | Google ads SocialAccount id.
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID, digits only). Defaults to the account's connected customer. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId, kept for existing callers (optional) 
            var fromDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Defaults to 30 days ago. (optional) 
            var toDate = DateOnly.Parse("2013-10-20");  // DateOnly? | Defaults to today. (optional) 

            try
            {
                // List portfolio bid strategies
                ListBidStrategies200Response result = apiInstance.ListBidStrategies(accountId, adAccountId, customerId, fromDate, toDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListBidStrategies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBidStrategiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List portfolio bid strategies
    ApiResponse<ListBidStrategies200Response> response = apiInstance.ListBidStrategiesWithHttpInfo(accountId, adAccountId, customerId, fromDate, toDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListBidStrategiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Google ads SocialAccount id. |  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID, digits only). Defaults to the account&#39;s connected customer. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId, kept for existing callers | [optional]  |
| **fromDate** | **DateOnly?** | Defaults to 30 days ago. | [optional]  |
| **toDate** | **DateOnly?** | Defaults to today. | [optional]  |

### Return type

[**ListBidStrategies200Response**](ListBidStrategies200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Portfolio bid strategies |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget exhausted; retry later. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignassets"></a>
# **ListCampaignAssets**
> ListCampaignAssets200Response ListCampaignAssets (string campaignId, string accountId, string? adAccountId = null, string? customerId = null)

List campaign assets

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

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
    public class ListCampaignAssetsExample
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
            var campaignId = "campaignId_example";  // string | Numeric Google platform id.
            var accountId = "accountId_example";  // string | 
            var adAccountId = "adAccountId_example";  // string? |  (optional) 
            var customerId = "customerId_example";  // string? |  (optional) 

            try
            {
                // List campaign assets
                ListCampaignAssets200Response result = apiInstance.ListCampaignAssets(campaignId, accountId, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListCampaignAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaign assets
    ApiResponse<ListCampaignAssets200Response> response = apiInstance.ListCampaignAssetsWithHttpInfo(campaignId, accountId, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListCampaignAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Numeric Google platform id. |  |
| **accountId** | **string** |  |  |
| **adAccountId** | **string?** |  | [optional]  |
| **customerId** | **string?** |  | [optional]  |

### Return type

[**ListCampaignAssets200Response**](ListCampaignAssets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignnegativekeywordlists"></a>
# **ListCampaignNegativeKeywordLists**
> ListAdNegativeKeywordLists200Response ListCampaignNegativeKeywordLists (string campaignId, string? platform = null)

List campaign negative lists

Returns shared negative keyword lists attached to the campaign, separate from campaign-level negative keywords. Google Ads shared negative keyword lists (shared_set type NEGATIVE_KEYWORDS). Reads are cached for 10 minutes; quota exhaustion may return the last successful result for up to 7 days with stale=true. Customer selection is limited to this connection and its account scope.

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
    public class ListCampaignNegativeKeywordListsExample
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
            var campaignId = "campaignId_example";  // string | 
            var platform = "facebook";  // string? |  (optional) 

            try
            {
                // List campaign negative lists
                ListAdNegativeKeywordLists200Response result = apiInstance.ListCampaignNegativeKeywordLists(campaignId, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListCampaignNegativeKeywordLists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignNegativeKeywordListsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaign negative lists
    ApiResponse<ListAdNegativeKeywordLists200Response> response = apiInstance.ListCampaignNegativeKeywordListsWithHttpInfo(campaignId, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListCampaignNegativeKeywordListsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** |  |  |
| **platform** | **string?** |  | [optional]  |

### Return type

[**ListAdNegativeKeywordLists200Response**](ListAdNegativeKeywordLists200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcampaignnegativekeywords"></a>
# **ListCampaignNegativeKeywords**
> ListCampaignNegativeKeywords200Response ListCampaignNegativeKeywords (string campaignId, string? platform = null)

List campaign-level negative keywords

Returns the campaign-level negative keywords (`campaign_criterion.negative`), distinct from the ad-group-level negatives under `GET /v1/ads/keywords`. Cached for the quota window (not synced to Postgres), and gated by the shared Google Ads operations budget like every other on-demand Google surface. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read.  The platform is always discovered from the campaign itself; a non-Google campaign returns 501 rather than 404, whether or not `platform` was passed. 

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
    public class ListCampaignNegativeKeywordsExample
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
            var platform = "facebook";  // string? | Optional and NOT authoritative: the resolved campaign's own platform decides 200 vs 501, never this hint. (optional) 

            try
            {
                // List campaign-level negative keywords
                ListCampaignNegativeKeywords200Response result = apiInstance.ListCampaignNegativeKeywords(campaignId, platform);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListCampaignNegativeKeywords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCampaignNegativeKeywordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List campaign-level negative keywords
    ApiResponse<ListCampaignNegativeKeywords200Response> response = apiInstance.ListCampaignNegativeKeywordsWithHttpInfo(campaignId, platform);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListCampaignNegativeKeywordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Platform campaign ID |  |
| **platform** | **string?** | Optional and NOT authoritative: the resolved campaign&#39;s own platform decides 200 vs 501, never this hint. | [optional]  |

### Return type

[**ListCampaignNegativeKeywords200Response**](ListCampaignNegativeKeywords200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign-level negative keywords |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Campaign not found |  -  |
| **429** | Google Ads operations budget exhausted; retry later |  -  |
| **501** | Only available on Google Ads campaigns |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listgoogleassetgroups"></a>
# **ListGoogleAssetGroups**
> ListGoogleAssetGroups200Response ListGoogleAssetGroups (string campaignId)

List Performance Max asset groups

Read Performance Max asset groups and their linked text, image and YouTube assets. campaignId is the platform campaign id returned by creation or the campaign list. The campaign must be visible to the caller. Uses a 10-minute cache, with the last successful response served as stale when Google quota is exhausted. Removed groups and asset links are excluded. Campaign-level brand assets on campaigns with brand guidelines enabled are not included.

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
    public class ListGoogleAssetGroupsExample
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
            var campaignId = "campaignId_example";  // string | Google Ads campaign id.

            try
            {
                // List Performance Max asset groups
                ListGoogleAssetGroups200Response result = apiInstance.ListGoogleAssetGroups(campaignId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListGoogleAssetGroups: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListGoogleAssetGroupsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Performance Max asset groups
    ApiResponse<ListGoogleAssetGroups200Response> response = apiInstance.ListGoogleAssetGroupsWithHttpInfo(campaignId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListGoogleAssetGroupsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google Ads campaign id. |  |

### Return type

[**ListGoogleAssetGroups200Response**](ListGoogleAssetGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Asset groups and linked assets. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **429** | Google quota or operation budget exhausted with no cached response. |  -  |
| **501** | Campaign is not on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listgooglerecommendations"></a>
# **ListGoogleRecommendations**
> ListGoogleRecommendations200Response ListGoogleRecommendations (string accountId, string? adAccountId = null, string? customerId = null, string? campaignId = null, string? types = null)

List Google Ads recommendations

Google's optimization recommendations for one ad account: type, estimated impact (base vs potential metrics, cost in account currency units), the campaign, ad group or budget they target, and the type-specific payload Google returns (`details`, in Google's own shape with micros). Filter by campaignId and types. Cached for 10 minutes and cleared by apply or dismiss; served stale when Google quota is exhausted.

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
    public class ListGoogleRecommendationsExample
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
            var accountId = "accountId_example";  // string | Google ads SocialAccount id.
            var adAccountId = "adAccountId_example";  // string? | Google customer id, digits only. Defaults to the connection's only customer. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId, kept for consistency with other Google endpoints. (optional) 
            var campaignId = "campaignId_example";  // string? | Only recommendations targeting this campaign. (optional) 
            var types = "types_example";  // string? | Comma-separated Google RecommendationType values, for example CAMPAIGN_BUDGET,KEYWORD,SET_TARGET_CPA. (optional) 

            try
            {
                // List Google Ads recommendations
                ListGoogleRecommendations200Response result = apiInstance.ListGoogleRecommendations(accountId, adAccountId, customerId, campaignId, types);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListGoogleRecommendations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListGoogleRecommendationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Google Ads recommendations
    ApiResponse<ListGoogleRecommendations200Response> response = apiInstance.ListGoogleRecommendationsWithHttpInfo(accountId, adAccountId, customerId, campaignId, types);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListGoogleRecommendationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Google ads SocialAccount id. |  |
| **adAccountId** | **string?** | Google customer id, digits only. Defaults to the connection&#39;s only customer. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId, kept for consistency with other Google endpoints. | [optional]  |
| **campaignId** | **string?** | Only recommendations targeting this campaign. | [optional]  |
| **types** | **string?** | Comma-separated Google RecommendationType values, for example CAMPAIGN_BUDGET,KEYWORD,SET_TARGET_CPA. | [optional]  |

### Return type

[**ListGoogleRecommendations200Response**](ListGoogleRecommendations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Recommendations. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | No Google Ads customer on this connection, or it needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | accountId is not a Google Ads connection. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listsharedbudgets"></a>
# **ListSharedBudgets**
> ListSharedBudgets200Response ListSharedBudgets (string accountId, string? adAccountId = null)

List shared budgets

Lists the Google Ads customer's shared campaign budgets (`campaign_budget.explicitly_shared` = true, not removed), with how many campaigns use each. Move a campaign onto one with `sharedBudgetId` on PUT /v1/ads/campaigns/{campaignId}. Google only; other platforms return 501. 

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
    public class ListSharedBudgetsExample
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
            var accountId = "accountId_example";  // string | Google ads SocialAccount id.
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID, digits only). Defaults to the account's connected customer. (optional) 

            try
            {
                // List shared budgets
                ListSharedBudgets200Response result = apiInstance.ListSharedBudgets(accountId, adAccountId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ListSharedBudgets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSharedBudgetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List shared budgets
    ApiResponse<ListSharedBudgets200Response> response = apiInstance.ListSharedBudgetsWithHttpInfo(accountId, adAccountId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ListSharedBudgetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **accountId** | **string** | Google ads SocialAccount id. |  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID, digits only). Defaults to the account&#39;s connected customer. | [optional]  |

### Return type

[**ListSharedBudgets200Response**](ListSharedBudgets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shared budgets |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeadgroupassets"></a>
# **RemoveAdGroupAssets**
> RemoveCampaignAssets200Response RemoveAdGroupAssets (string adSetId, string accountId, List<string> assetResourceNames, List<string> adGroupAssetResourceNames, string? adAccountId = null, string? customerId = null)

Remove ad-group assets

Removes the specified attachments only. Google assets cannot be deleted. Other attachments remain. assetResourceNames is retained for compatibility. Fields go in the query string. A JSON body with the same fields is also accepted and, when sent, the query string is ignored.

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
    public class RemoveAdGroupAssetsExample
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
            var adSetId = "adSetId_example";  // string | Numeric Google platform id.
            var accountId = "accountId_example";  // string | Zernio Google Ads connection id.
            var assetResourceNames = new List<string>(); // List<string> | Asset resource names, retained for compatibility. Repeat the parameter or pass a comma-separated list.
            var adGroupAssetResourceNames = new List<string>(); // List<string> | ad_group_asset resource names to remove, e.g. customers/1234567890/adGroupAssets/456~123~CALLOUT. Repeat the parameter or pass a comma-separated list.
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId, kept for existing callers (optional) 

            try
            {
                // Remove ad-group assets
                RemoveCampaignAssets200Response result = apiInstance.RemoveAdGroupAssets(adSetId, accountId, assetResourceNames, adGroupAssetResourceNames, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.RemoveAdGroupAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveAdGroupAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove ad-group assets
    ApiResponse<RemoveCampaignAssets200Response> response = apiInstance.RemoveAdGroupAssetsWithHttpInfo(adSetId, accountId, assetResourceNames, adGroupAssetResourceNames, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.RemoveAdGroupAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Numeric Google platform id. |  |
| **accountId** | **string** | Zernio Google Ads connection id. |  |
| **assetResourceNames** | [**List&lt;string&gt;**](string.md) | Asset resource names, retained for compatibility. Repeat the parameter or pass a comma-separated list. |  |
| **adGroupAssetResourceNames** | [**List&lt;string&gt;**](string.md) | ad_group_asset resource names to remove, e.g. customers/1234567890/adGroupAssets/456~123~CALLOUT. Repeat the parameter or pass a comma-separated list. |  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId, kept for existing callers | [optional]  |

### Return type

[**RemoveCampaignAssets200Response**](RemoveCampaignAssets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removeadkeyword"></a>
# **RemoveAdKeyword**
> RemoveAdKeyword200Response RemoveAdKeyword (string keywordId)

Remove a Search keyword

Removes one keyword criterion (positive or negative) from its ad group (M.140).

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
    public class RemoveAdKeywordExample
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
            var keywordId = "keywordId_example";  // string | Zernio keyword ID (`id`), or Google's native `{adSetId}~{platformCriterionId}` (the tail of `resourceName`, e.g. 1234567890~987654321). A bare criterion id is rejected because it is only unique within its ad group.

            try
            {
                // Remove a Search keyword
                RemoveAdKeyword200Response result = apiInstance.RemoveAdKeyword(keywordId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.RemoveAdKeyword: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveAdKeywordWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a Search keyword
    ApiResponse<RemoveAdKeyword200Response> response = apiInstance.RemoveAdKeywordWithHttpInfo(keywordId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.RemoveAdKeywordWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **keywordId** | **string** | Zernio keyword ID (&#x60;id&#x60;), or Google&#39;s native &#x60;{adSetId}~{platformCriterionId}&#x60; (the tail of &#x60;resourceName&#x60;, e.g. 1234567890~987654321). A bare criterion id is rejected because it is only unique within its ad group. |  |

### Return type

[**RemoveAdKeyword200Response**](RemoveAdKeyword200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Keyword removed |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removecampaignassets"></a>
# **RemoveCampaignAssets**
> RemoveCampaignAssets200Response RemoveCampaignAssets (string campaignId, string accountId, List<string> assetResourceNames, List<string> campaignAssetResourceNames, string? adAccountId = null, string? customerId = null)

Remove campaign assets

Removes the specified attachments only. Google assets cannot be deleted. Other attachments remain. assetResourceNames is retained for compatibility. Fields go in the query string. A JSON body with the same fields is also accepted and, when sent, the query string is ignored.

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
    public class RemoveCampaignAssetsExample
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
            var campaignId = "campaignId_example";  // string | Numeric Google platform id.
            var accountId = "accountId_example";  // string | Zernio Google Ads connection id.
            var assetResourceNames = new List<string>(); // List<string> | Asset resource names, retained for compatibility. Repeat the parameter or pass a comma-separated list.
            var campaignAssetResourceNames = new List<string>(); // List<string> | campaign_asset resource names to remove, e.g. customers/1234567890/campaignAssets/456~123~CALLOUT. Repeat the parameter or pass a comma-separated list.
            var adAccountId = "adAccountId_example";  // string? | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. (optional) 
            var customerId = "customerId_example";  // string? | Alias of adAccountId, kept for existing callers (optional) 

            try
            {
                // Remove campaign assets
                RemoveCampaignAssets200Response result = apiInstance.RemoveCampaignAssets(campaignId, accountId, assetResourceNames, campaignAssetResourceNames, adAccountId, customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.RemoveCampaignAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveCampaignAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove campaign assets
    ApiResponse<RemoveCampaignAssets200Response> response = apiInstance.RemoveCampaignAssetsWithHttpInfo(campaignId, accountId, assetResourceNames, campaignAssetResourceNames, adAccountId, customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.RemoveCampaignAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Numeric Google platform id. |  |
| **accountId** | **string** | Zernio Google Ads connection id. |  |
| **assetResourceNames** | [**List&lt;string&gt;**](string.md) | Asset resource names, retained for compatibility. Repeat the parameter or pass a comma-separated list. |  |
| **campaignAssetResourceNames** | [**List&lt;string&gt;**](string.md) | campaign_asset resource names to remove, e.g. customers/1234567890/campaignAssets/456~123~CALLOUT. Repeat the parameter or pass a comma-separated list. |  |
| **adAccountId** | **string?** | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. | [optional]  |
| **customerId** | **string?** | Alias of adAccountId, kept for existing callers | [optional]  |

### Return type

[**RemoveCampaignAssets200Response**](RemoveCampaignAssets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="removegoogleassetgroup"></a>
# **RemoveGoogleAssetGroup**
> RemoveGoogleAssetGroup200Response RemoveGoogleAssetGroup (string campaignId, string assetGroupId, bool? validateOnly = null)

Remove a Performance Max asset group

Removes the asset group on Google (status REMOVED, not reversible). Pass validateOnly=true to validate without removing.

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
    public class RemoveGoogleAssetGroupExample
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
            var campaignId = "campaignId_example";  // string | 
            var assetGroupId = "assetGroupId_example";  // string | 
            var validateOnly = false;  // bool? |  (optional)  (default to false)

            try
            {
                // Remove a Performance Max asset group
                RemoveGoogleAssetGroup200Response result = apiInstance.RemoveGoogleAssetGroup(campaignId, assetGroupId, validateOnly);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.RemoveGoogleAssetGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveGoogleAssetGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove a Performance Max asset group
    ApiResponse<RemoveGoogleAssetGroup200Response> response = apiInstance.RemoveGoogleAssetGroupWithHttpInfo(campaignId, assetGroupId, validateOnly);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.RemoveGoogleAssetGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** |  |  |
| **assetGroupId** | **string** |  |  |
| **validateOnly** | **bool?** |  | [optional] [default to false] |

### Return type

[**RemoveGoogleAssetGroup200Response**](RemoveGoogleAssetGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Removed (or validated). |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | Google Ads connection needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | Campaign is not on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replacecampaignnegativekeywordlists"></a>
# **ReplaceCampaignNegativeKeywordLists**
> ReplaceAdNegativeKeywordListKeywords200Response ReplaceCampaignNegativeKeywordLists (string campaignId, ReplaceCampaignNegativeKeywordListsRequest replaceCampaignNegativeKeywordListsRequest)

Replace campaign negative lists

Sets the full desired set of shared negative keyword list associations on this campaign. Send listIds=[] to detach all negative keyword lists. Only campaign_shared_set links are changed; the lists and their keywords are preserved. Every list must belong to the campaign customer and have type NEGATIVE_KEYWORDS.

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
    public class ReplaceCampaignNegativeKeywordListsExample
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
            var campaignId = "campaignId_example";  // string | 
            var replaceCampaignNegativeKeywordListsRequest = new ReplaceCampaignNegativeKeywordListsRequest(); // ReplaceCampaignNegativeKeywordListsRequest | 

            try
            {
                // Replace campaign negative lists
                ReplaceAdNegativeKeywordListKeywords200Response result = apiInstance.ReplaceCampaignNegativeKeywordLists(campaignId, replaceCampaignNegativeKeywordListsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ReplaceCampaignNegativeKeywordLists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplaceCampaignNegativeKeywordListsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace campaign negative lists
    ApiResponse<ReplaceAdNegativeKeywordListKeywords200Response> response = apiInstance.ReplaceCampaignNegativeKeywordListsWithHttpInfo(campaignId, replaceCampaignNegativeKeywordListsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ReplaceCampaignNegativeKeywordListsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** |  |  |
| **replaceCampaignNegativeKeywordListsRequest** | [**ReplaceCampaignNegativeKeywordListsRequest**](ReplaceCampaignNegativeKeywordListsRequest.md) |  |  |

### Return type

[**ReplaceAdNegativeKeywordListKeywords200Response**](ReplaceAdNegativeKeywordListKeywords200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access and permission to the selected account are required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Ambiguous campaign or account selection. Use a profile-scoped key. A list still attached to a campaign may also be rejected by Google. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **422** | Google Ads connection is missing or unavailable. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Available only on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replacecampaignnegativekeywords"></a>
# **ReplaceCampaignNegativeKeywords**
> ReplaceCampaignNegativeKeywords200Response ReplaceCampaignNegativeKeywords (string campaignId, ReplaceCampaignNegativeKeywordsRequest replaceCampaignNegativeKeywordsRequest)

Replace campaign-level negative keywords

Replaces the FULL set of campaign-level negative keywords (C.270): the desired list is diffed against what Google already has, and the difference is applied as one `create`/`remove` mutate. Send an empty array to clear every campaign negative.  The platform is always discovered from the campaign itself; a non-Google campaign returns 501 rather than 404, whether or not `platform` was sent. 

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
    public class ReplaceCampaignNegativeKeywordsExample
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
            var replaceCampaignNegativeKeywordsRequest = new ReplaceCampaignNegativeKeywordsRequest(); // ReplaceCampaignNegativeKeywordsRequest | 

            try
            {
                // Replace campaign-level negative keywords
                ReplaceCampaignNegativeKeywords200Response result = apiInstance.ReplaceCampaignNegativeKeywords(campaignId, replaceCampaignNegativeKeywordsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ReplaceCampaignNegativeKeywords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplaceCampaignNegativeKeywordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace campaign-level negative keywords
    ApiResponse<ReplaceCampaignNegativeKeywords200Response> response = apiInstance.ReplaceCampaignNegativeKeywordsWithHttpInfo(campaignId, replaceCampaignNegativeKeywordsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ReplaceCampaignNegativeKeywordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Platform campaign ID |  |
| **replaceCampaignNegativeKeywordsRequest** | [**ReplaceCampaignNegativeKeywordsRequest**](ReplaceCampaignNegativeKeywordsRequest.md) |  |  |

### Return type

[**ReplaceCampaignNegativeKeywords200Response**](ReplaceCampaignNegativeKeywords200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign-level negative keywords replaced |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Campaign not found |  -  |
| **429** | Google Ads operations budget exhausted; retry later |  -  |
| **501** | Only available on Google Ads campaigns |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="replacegooglelistinggroupfilters"></a>
# **ReplaceGoogleListingGroupFilters**
> ReplaceGoogleListingGroupFilters200Response ReplaceGoogleListingGroupFilters (string campaignId, string assetGroupId, ReplaceGoogleListingGroupFiltersRequest replaceGoogleListingGroupFiltersRequest)

Replace an asset group's listing-group tree

Replace the product (listing-group) tree of a Performance Max retail asset group. The current tree is removed and the new one created in one atomic request. Read the current tree with GET on the asset group. Requires a campaign linked to Merchant Center; other campaigns return 400 LISTING_SOURCE_NOT_ALLOWED from Google. validateOnly: true validates without writing.

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
    public class ReplaceGoogleListingGroupFiltersExample
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
            var campaignId = "campaignId_example";  // string | Google Ads campaign id.
            var assetGroupId = "assetGroupId_example";  // string | Google asset group id.
            var replaceGoogleListingGroupFiltersRequest = new ReplaceGoogleListingGroupFiltersRequest(); // ReplaceGoogleListingGroupFiltersRequest | 

            try
            {
                // Replace an asset group's listing-group tree
                ReplaceGoogleListingGroupFilters200Response result = apiInstance.ReplaceGoogleListingGroupFilters(campaignId, assetGroupId, replaceGoogleListingGroupFiltersRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.ReplaceGoogleListingGroupFilters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplaceGoogleListingGroupFiltersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace an asset group's listing-group tree
    ApiResponse<ReplaceGoogleListingGroupFilters200Response> response = apiInstance.ReplaceGoogleListingGroupFiltersWithHttpInfo(campaignId, assetGroupId, replaceGoogleListingGroupFiltersRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.ReplaceGoogleListingGroupFiltersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google Ads campaign id. |  |
| **assetGroupId** | **string** | Google asset group id. |  |
| **replaceGoogleListingGroupFiltersRequest** | [**ReplaceGoogleListingGroupFiltersRequest**](ReplaceGoogleListingGroupFiltersRequest.md) |  |  |

### Return type

[**ReplaceGoogleListingGroupFilters200Response**](ReplaceGoogleListingGroupFilters200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tree replaced (or validated). |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | Google Ads connection needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | Campaign is not on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatead"></a>
# **UpdateAd**
> UpdateAd200Response UpdateAd (string adId, UpdateAdRequest updateAdRequest)

Update ad

Patch one or more fields on an ad. Status, budget, targeting, and creative changes are propagated to the platform.  Per-platform support: - **Meta** (Facebook + Instagram): all fields supported. - **TikTok**: status, budget, `name` (renames the ad), targeting (via `/v2/adgroup/update/`), and creative   (via `/v2/ad/update/` patch-style: `headline` is ignored, `body` becomes `ad_text`). - **Google**: status, budget, KEYWORD edits via `targeting.keywords` /   `targeting.negativeKeywords`, DEVICE bid adjustments via `targeting.devices`,   LOCATION edits via `targeting.locations` (or the equivalent top-level   `targeting.countries` / `regions` / `cities` / `zips` / `metros`), and LANGUAGE   edits via `targeting.languages`.   Each list you send becomes the FULL new set of its kind (criteria not in the   list are removed, except devices, which Google cannot remove and which are   switched off with a bid modifier of 0 instead); a kind left out is untouched.   Any other `targeting` field   returns 400: Google cannot mutate it post-create without recreating   the campaign. Creative edits are dispatched on the ad's `advertisingChannelType`,   and every supported field replaces a whole set; a field you omit is preserved.   - **Search**: top-level `headlines`, `descriptions` and `finalUrls`. Use 3-15 headlines     (1-30 characters) and 2-4 descriptions (1-90 characters). Omit an asset to remove it;     omit pinnedField on an included asset to unpin it. Updates do not pad or truncate text.     The legacy creative fields remain unsupported.   - **Display**: top-level `headlines` (1-5, no pinnedField, display ads have no pinned     positions), `descriptions` (1-5) and `finalUrls`, plus `creative.longHeadline`,     `creative.businessName`, `creative.imageUrl` (the landscape marketing image) and     `creative.squareImageUrl`. Each image URL is uploaded as a new Google asset and the ad     is pointed at it; Google assets are immutable, so the previous asset stays in the     account's asset library.   - **Performance Max**: top-level `assetGroup`, which swaps asset roles on the ad's asset     group. The other creative fields return 422 for this channel, and `assetGroup` returns     422 on any other channel.   - **Demand Gen**: top-level `demandGen` (see GoogleDemandGenUpdate): creative, channel     and audience changes in one atomic Google request. The other creative fields return     422 for this channel. `targeting` takes locations, languages, `locationTargetingType`     and `devices`; locations and languages are written to the ad's ad group, which     Demand Gen requires (campaigns migrated from Discovery that still target on the     campaign keep being written there), so they apply to every ad in that ad group. - **LinkedIn**: status, budget, targeting (countries or regions, excludedLocations (countries),   the B2B facets, and audience segments; applied to the LinkedIn Campaign via   PARTIAL_UPDATE, and REPLACES the campaign's entire targetingCriteria, not a merge),   and creative (uploads new media, creates a replacement inline creative on the same   campaign, pauses the old one). - **Pinterest / X / OpenAI Ads**: status + budget only. Sending   `targeting` or `creative` returns 501 with code `unsupported_platform_operation`.   OpenAI Ads budget is the campaign's spend cap, daily or lifetime (see `budget.type` below).  **Google location and language replacement:** locations, languages and devices are campaign-level criteria on Google, so these edits apply to every ad group and ad in the ad's campaign. Send the complete list you want to keep. Zernio diffs it against the campaign's live criteria and sends the removes and the creates in ONE `googleAds:mutate`, so the campaign is never left with a half-applied set; criteria already in the list keep their criterion ID and history. Excluded (negative) locations are left untouched. An empty location list returns 400 (a Google campaign with no location criteria targets every country, which is never what \"remove my locations\" means, so omit the field instead). Send either `targeting.locations` or the top-level geo fields, not both: mixing them returns 400.  **Google radius targeting:** `customLocations` is editable and is replaced the same way, but as its OWN set. Google models a place (LOCATION) and a point plus radius (PROXIMITY) as different criterion types, so the two are independent: sending `customLocations` replaces every radius and leaves the cities and countries alone, and sending places replaces those and leaves the radius alone. Send `customLocations: []` to drop radius targeting entirely. A circle you re-send unchanged keeps its criterion ID rather than being removed and recreated.  **Google keyword replacement:** These edits affect the ad's entire ad group, including sibling ads. Positive (`targeting.keywords`) and negative (`targeting.negativeKeywords`) sets are independent: omit a field to leave that set unchanged, or send `[]` to remove every keyword of that kind.  Zernio compares each supplied set with Google's live criteria by case-insensitive keyword text and match type. A matching criterion is left untouched, retaining its criterion ID, enabled/paused status, keyword-level bid overrides, labels, and criterion-associated history/statistics. Zernio does not reset its quality score; Google continues to calculate scores and statistics normally. Text comparison does not trim whitespace.  A bare string or an object without `matchType` means `broad`, not the existing criterion's match type. For example, resending an existing `{ \"text\": \"plumber\", \"matchType\": \"exact\" }` preserves it; sending `\"plumber\"` instead removes that EXACT criterion and requests a BROAD one. Changing text or match type removes criteria no longer requested and creates any missing criteria. New criteria get new IDs and do not inherit removed criteria's bid overrides, labels, or history. Historical reporting for a removed criterion is not transferred to its replacement.  To add keywords without replacing a set, use [POST /v1/ads/keywords](https://docs.zernio.com/ad-campaigns/add-ad-keywords). Use `PATCH /v1/ads/keywords/{keywordId}` to pause/enable one keyword, or `DELETE /v1/ads/keywords/{keywordId}` to remove it. 

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
| **400** | Invalid status transition, budget below minimum, a LinkedIn creative update without imageUrl or videoUrl, a LinkedIn targeting update without countries or regions, or a Google targeting update that is unsupported, empty, mixes locations with the top-level geo fields, or names an unknown country or language code |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Resource not found |  -  |
| **422** | The ad has no campaign or ad group on the platform yet, the Google targeting edit asks for something that is create-only (&#x60;locations.customLocations&#x60;), or a creative field the ad&#39;s channel cannot carry: assetGroup on a non-Performance-Max ad, a Google Display field on a Search ad, a pinnedField on a Display headline, or any Google-only field on another platform. A Google creative edit that cannot reach Google at all (the ad has no &#x60;platformAdId&#x60;, or its ad account cannot be loaded) also returns 422 rather than a 200 that changed nothing. |  -  |
| **429** | Meta admits one write per 30 seconds to a metered object, ad creatives above all. Zernio waits out two of those windows and replays the call before surfacing this, so it only appears when the object is being edited faster than that. Retry in 30 seconds. |  -  |
| **501** | targeting or creative not supported on the platform (supported on Meta, TikTok, and LinkedIn) |  -  |
| **502** | Meta accepted the request then failed to produce the media (upload session, chunk transfer, processing timeout, or a response with no image hash). Inspect &#x60;platformError.reason&#x60;. Also returned with code &#x60;platform_api_error&#x60; when a Meta or LinkedIn targeting update cannot read the current targeting: nothing is written, so retry the request. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadcampaign"></a>
# **UpdateAdCampaign**
> UpdateAdCampaign200Response UpdateAdCampaign (string campaignId, UpdateAdCampaignRequest updateAdCampaignRequest)

Update a campaign

Campaign-level edits. Send at least one of `budget`, `bidStrategy`, `portfolioBidStrategyId`, `targetImpressionShare`, `manualCpc`, `networkSettings`, `trackingUrlTemplate`, `finalUrlSuffix`, `sharedBudgetId`, `name` or `platformSpecificData`. An unsupported field is always an error, never a silent drop.  | Body field | Meta | Google | Others | |- --|- --|- --|- --| | `bidStrategy` | Yes | Yes | 501 | | `bidAmount`, `roasAverageFloor` | 400 (ad-set level) | Yes | 400 | | `portfolioBidStrategyId` | 400 | Yes | 400 | | `targetImpressionShare` | 400 | Search only | 400 | | `manualCpc` | 400 | Search and Display | 400 | | `networkSettings` | 400 | Search only | 400 | | `trackingUrlTemplate`, `finalUrlSuffix` | 400 | Yes | 400 | | `sharedBudgetId` | 400 | Yes | 400 | | `budget` (CBO; ABO returns 409) | Yes | Daily only | OpenAI: daily or lifetime; others 501 | | `name` | Yes | 501 | 501 | | `platformSpecificData.spendCap` | Yes | 400 | 400 | | `accountId` (empty campaigns) | Yes | - | - |  Meta budget edits check the live campaign budget, so an older local ABO stamp cannot block a CBO campaign. A successful edit repairs local ad budget fields. A live ABO campaign still returns 409 with the ad-set budget endpoint.  On Google: `LOWEST_COST_WITHOUT_CAP` = Maximize Conversions, `COST_CAP` + `bidAmount` = Target CPA, `LOWEST_COST_WITH_MIN_ROAS` + `roasAverageFloor` = Target ROAS, `LOWEST_COST_WITH_BID_CAP` + `bidAmount` = Maximize Clicks with a CPC ceiling; `portfolioBidStrategyId` attaches a portfolio strategy instead (exclusive with `bidStrategy`). `targetImpressionShare` switches the campaign to Target impression share and `manualCpc: { maxCpc }` to Manual CPC (every ad group of the campaign gets `maxCpc` as its bid, in the same mutate); each is exclusive with every other strategy field. `networkSettings`, `trackingUrlTemplate` and `finalUrlSuffix` go out in one campaign update, each field sent written on its own leaf, so an omitted one keeps its current value; an empty string clears a URL field. Setting the standard triplet on a campaign that is currently on a PORTFOLIO strategy is rejected: detach it in Google Ads first, since it is shared across campaigns.  Google budget updates read the current budget before mutation. Shared budgets return 409 unless allowSharedBudgetUpdate=true is explicitly supplied, because the change affects every campaign using that budget. Unknown sharing state also returns 409.  `sharedBudgetId` (Google) moves the campaign onto a shared budget from GET /v1/ads/shared-budgets, which also needs `allowSharedBudgetUpdate: true` (409 otherwise) because the campaign then splits that budget with every campaign on it; `budget` cannot ride along. `sharedBudgetId: null` moves it back onto a new budget of its own, sized by `budget` (required, daily); the new budget and the switch go out in one atomic Google mutate. A campaign that already has its own budget returns 409 for null. The budget a campaign leaves is not removed. The response carries the budget the campaign now uses.  OpenAI Ads campaigns carry exactly one spend cap: `budget.type` daily or lifetime replaces whichever cap the campaign had, with a minimum of 1 in the ad account's currency (422 below it). Lifetime can switch to daily, but OpenAI never switches a daily cap back to lifetime (422).  `accountId` forwards the update straight to Meta for a campaign with zero ads, which would otherwise 404; the response then carries `updated: 0`. 

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | Meta campaign is ABO, or the Google budget is shared without allowSharedBudgetUpdate&#x3D;true, or sharing state cannot be verified. The account may also be inactive or need reconnection (code ads_connection_required). Reconnect it and read GET /v1/accounts for its current ID before retrying. |  -  |
| **501** | Operation not supported on this platform |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadcampaignstatus"></a>
# **UpdateAdCampaignStatus**
> UpdateAdCampaignStatus200Response UpdateAdCampaignStatus (string campaignId, UpdateAdCampaignStatusRequest updateAdCampaignStatusRequest)

Pause or resume a campaign

Writes the campaign's own on/off switch and nothing else, on every platform (Meta, TikTok, Google, LinkedIn campaign group, Pinterest, X, ChatGPT (OpenAI)). Its ad sets and ads keep their own switches: pausing stops their delivery through the campaign, and resuming lets each of them deliver again only if its own switch is on. An ad set or ad you paused individually stays paused; resume it with PUT /v1/ads/ad-sets/{adSetId}/status or PUT /v1/ads/{adId}/status. See the Status model in the Ad Campaigns tag.  **Live read, then write.** The campaign's switch is read from the platform first. When that live read shows it already in the requested state nothing is written (`updated: 0`, `skipped: 1`, with the reason). Otherwise the switch is written (`updated: 1`), read back and stored, and the delivery status of the ads under it (up to 20) is re-read and stored, so an immediate GET returns what the platform now reports. A stored switch never skips a write, and when the platform cannot be read the write always goes out. On Meta the check reads the campaign's own `status`, so a delivery status such as `IN_PROCESS` or `WITH_ISSUES` does not force a write. 

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
| **400** | Invalid input or campaign spans multiple accounts |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | No ads found for this campaign |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadgroupassets"></a>
# **UpdateAdGroupAssets**
> UpdateCampaignAssets200Response UpdateAdGroupAssets (string adSetId, UpdateCampaignAssetsRequest updateCampaignAssetsRequest)

Update ad-group assets

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

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
    public class UpdateAdGroupAssetsExample
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
            var adSetId = "adSetId_example";  // string | Numeric Google platform id.
            var updateCampaignAssetsRequest = new UpdateCampaignAssetsRequest(); // UpdateCampaignAssetsRequest | 

            try
            {
                // Update ad-group assets
                UpdateCampaignAssets200Response result = apiInstance.UpdateAdGroupAssets(adSetId, updateCampaignAssetsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAdGroupAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdGroupAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update ad-group assets
    ApiResponse<UpdateCampaignAssets200Response> response = apiInstance.UpdateAdGroupAssetsWithHttpInfo(adSetId, updateCampaignAssetsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdGroupAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adSetId** | **string** | Numeric Google platform id. |  |
| **updateCampaignAssetsRequest** | [**UpdateCampaignAssetsRequest**](UpdateCampaignAssetsRequest.md) |  |  |

### Return type

[**UpdateCampaignAssets200Response**](UpdateCampaignAssets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadkeyword"></a>
# **UpdateAdKeyword**
> UpdateAdKeyword200Response UpdateAdKeyword (string keywordId, UpdateAdKeywordRequest updateAdKeywordRequest)

Pause or enable a Search keyword

Changes `ad_group_criterion.status` for one keyword criterion (M.140). Negative keywords have no status on Google and cannot be paused or enabled. 

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
    public class UpdateAdKeywordExample
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
            var keywordId = "keywordId_example";  // string | Zernio keyword ID (`id`), or Google's native `{adSetId}~{platformCriterionId}` (the tail of `resourceName`, e.g. 1234567890~987654321). A bare criterion id is rejected because it is only unique within its ad group.
            var updateAdKeywordRequest = new UpdateAdKeywordRequest(); // UpdateAdKeywordRequest | 

            try
            {
                // Pause or enable a Search keyword
                UpdateAdKeyword200Response result = apiInstance.UpdateAdKeyword(keywordId, updateAdKeywordRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateAdKeyword: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdKeywordWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause or enable a Search keyword
    ApiResponse<UpdateAdKeyword200Response> response = apiInstance.UpdateAdKeywordWithHttpInfo(keywordId, updateAdKeywordRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateAdKeywordWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **keywordId** | **string** | Zernio keyword ID (&#x60;id&#x60;), or Google&#39;s native &#x60;{adSetId}~{platformCriterionId}&#x60; (the tail of &#x60;resourceName&#x60;, e.g. 1234567890~987654321). A bare criterion id is rejected because it is only unique within its ad group. |  |
| **updateAdKeywordRequest** | [**UpdateAdKeywordRequest**](UpdateAdKeywordRequest.md) |  |  |

### Return type

[**UpdateAdKeyword200Response**](UpdateAdKeyword200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Keyword updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **422** | Negative keywords have no status on Google; they cannot be paused or enabled. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadset"></a>
# **UpdateAdSet**
> UpdateAdSet200Response UpdateAdSet (string adSetId, UpdateAdSetRequest updateAdSetRequest)

Update an ad set

Ad-set-level writes. Use this for ABO budget updates, ad-set-scoped pause/resume, bid-strategy edits, Meta value-rule-set attach/detach, and Meta-only post-launch delivery settings via `platformSpecificData`. At least one updatable field is required.  Value rule sets (Meta only, see `/v1/ads/value-rule-sets`): - ATTACH or REPLACE: send `valueRuleSetId`. Attachment is driven by the id's   presence, so `valueRulesApplied: true` is optional. Sending a different id   replaces the previous association; there is no separate replace call. - DETACH: send `valueRulesApplied: false` and OMIT `valueRuleSetId`. - Sending `valueRulesApplied: false` TOGETHER with `valueRuleSetId` returns 400   `mutually_exclusive_fields`. This is deliberate: Meta attaches the rule set   whenever `value_rule_set_id` is present, even with `value_rules_applied` false,   so echoing stored state while asking to detach would silently keep the bid   adjustments live. - Eligibility: only ad sets on `LOWEST_COST_WITHOUT_CAP` or `COST_CAP`. Meta   rejects the rest server-side. - Read back with `GET /v1/ads/ad-sets/{adSetId}?fields=value_rule_set_id`. Meta   does not document `value_rules_applied` as a readable ad-set field, so the   boolean cannot be read back.  Bid strategy compatibility (per Meta's spec): - `LOWEST_COST_WITHOUT_CAP`: no `bidAmount`, no `roasAverageFloor`. - `LOWEST_COST_WITH_BID_CAP` / `COST_CAP`: `bidAmount` REQUIRED (whole currency units). - `LOWEST_COST_WITH_MIN_ROAS`: `roasAverageFloor` REQUIRED (decimal multiplier, e.g. 2.0 = 2.0x ROAS). - Meta only: send `bidAmount` WITHOUT `bidStrategy` to change the cap amount on an ad set   under a COST_CAP / LOWEST_COST_WITH_BID_CAP parent campaign, leaving the strategy itself   (inherited from the campaign) untouched. `roasAverageFloor` without `bidStrategy` is   rejected (it has no meaning outside LOWEST_COST_WITH_MIN_ROAS).  Delivery settings are validated by Meta against the campaign objective; incompatible combinations (e.g. a billingEvent the optimization goal doesn't allow) surface as 400s from Meta.  When updating `budget` on an ABO campaign: if the parent campaign is CBO, the response is 409 with code BUDGET_LEVEL_MISMATCH. Route to PUT /v1/ads/campaigns/{campaignId} instead.  `status` behaves exactly as PUT /v1/ads/ad-sets/{adSetId}/status describes: only the ad set's own switch is written, its ads keep theirs, and `statusUpdated` / `statusSkipped` report whether that switch was written or a live read showed it already in place. 

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Ad set not found |  -  |
| **409** | Campaign is CBO. Route to /v1/ads/campaigns/{campaignId} instead |  -  |
| **422** | bidStrategy is LOWEST_COST_WITH_MIN_ROAS on OpenAI (unsupported: no ROAS-based bidding) |  -  |
| **501** | bidStrategy not supported on the platform (Meta, TikTok, and OpenAI only) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadsetstatus"></a>
# **UpdateAdSetStatus**
> UpdateAdSetStatus200Response UpdateAdSetStatus (string adSetId, UpdateAdCampaignStatusRequest updateAdCampaignStatusRequest)

Pause or resume a single ad set

Ad-set-scoped pause/resume (doesn't touch sibling ad sets). Thin wrapper over PUT /v1/ads/ad-sets/{adSetId} for callers that only want the status toggle and prefer a symmetric URL to /v1/ads/campaigns/{campaignId}/status.  Writes the ad set's own on/off switch and nothing else, on every platform (Meta `configured_status`, TikTok ad group `operation_status`, Google ad group status, LinkedIn campaign, Pinterest ad group, X line item, ChatGPT (OpenAI) ad group). Its ads keep their own switches: an ad you paused individually stays paused when the ad set resumes. The campaign above is not touched either, so an ad set resumed under a paused campaign reads `status: paused` until the campaign is resumed too. See the Status model in the Ad Campaigns tag.  **Live read, then write.** The ad set's switch is read from the platform first. When that live read shows it already in the requested state nothing is written (`updated: 0`, `skipped: 1`, with the reason). Otherwise the switch is written (`updated: 1`), read back and stored, and the delivery status of its ads (up to 20) is re-read and stored, so an immediate GET returns what the platform now reports. A stored switch never skips a write, and when the platform cannot be read the write always goes out. On Meta the check reads the ad set's own `status`, so a repeated request skips even while `platformAdSetStatus` reads `CAMPAIGN_PAUSED`, `WITH_ISSUES` or `IN_PROCESS`. 

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Ad set not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateadstatus"></a>
# **UpdateAdStatus**
> UpdateAdStatus200Response UpdateAdStatus (string adId, UpdateAdKeywordRequest updateAdKeywordRequest)

Pause or resume a single ad

Ad-scoped pause/resume: flips ONLY this ad's own switch (Meta `configured_status`, TikTok `operation_status`, Google ad group ad status, LinkedIn creative, Pinterest ad), never its parent ad set or campaign, so sibling ads keep running. X is the exception: its smallest switch is the line item. Thin wrapper over the `status` field of PUT /v1/ads/{adId}, for callers that want a URL symmetric to /v1/ads/campaigns/{campaignId}/status and /v1/ads/ad-sets/{adSetId}/status.  The ad's own switch is independent of its delivery status. An ad paused only because its campaign or ad set is off (`status: paused`, `configuredStatus: ACTIVE`) can still be switched off here, and switching an ad on under a paused campaign leaves it `paused` until the campaign is resumed. After the write the switch is read back from the platform and returned as `configuredStatus`, together with the resulting delivery `status`.  `{adId}` accepts the same identifier dialects as GET/PUT /v1/ads/{adId} (Zernio hex `_id`, Meta numeric `platformAdId`, or the creative's effective story/media IDs). `platform` is inferred from the ad, so it's not required in the body. Ads in terminal statuses (rejected, completed, cancelled) are skipped, and so is a request whose target already matches the ad's own switch as read LIVE from the platform (a stored value is never trusted alone, since the switch may have been changed in the platform's own UI). A skip also returns that live read. The rolled-up `status` never decides a skip. 

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
            var updateAdKeywordRequest = new UpdateAdKeywordRequest(); // UpdateAdKeywordRequest | 

            try
            {
                // Pause or resume a single ad
                UpdateAdStatus200Response result = apiInstance.UpdateAdStatus(adId, updateAdKeywordRequest);
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
    ApiResponse<UpdateAdStatus200Response> response = apiInstance.UpdateAdStatusWithHttpInfo(adId, updateAdKeywordRequest);
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
| **updateAdKeywordRequest** | [**UpdateAdKeywordRequest**](UpdateAdKeywordRequest.md) |  |  |

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
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Ad not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebidstrategy"></a>
# **UpdateBidStrategy**
> UpdateBidStrategy200Response UpdateBidStrategy (string strategyId, UpdateBidStrategyRequest updateBidStrategyRequest)

Update portfolio bid strategy

Renames or retargets a portfolio bid strategy. The strategy's status is output only on Google's side, so it cannot be changed here; remove a strategy in Google Ads. `type` is only needed alongside `targetCpa`/`targetRoas` to disambiguate the field Google writes to (TARGET_CPA and MAXIMIZE_CONVERSIONS both take a target CPA; TARGET_ROAS and MAXIMIZE_CONVERSION_VALUE both take a target ROAS); the strategy's family is otherwise immutable once created.

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
    public class UpdateBidStrategyExample
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
            var strategyId = "strategyId_example";  // string | Numeric Google Ads bid strategy id.
            var updateBidStrategyRequest = new UpdateBidStrategyRequest(); // UpdateBidStrategyRequest | 

            try
            {
                // Update portfolio bid strategy
                UpdateBidStrategy200Response result = apiInstance.UpdateBidStrategy(strategyId, updateBidStrategyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateBidStrategy: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBidStrategyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update portfolio bid strategy
    ApiResponse<UpdateBidStrategy200Response> response = apiInstance.UpdateBidStrategyWithHttpInfo(strategyId, updateBidStrategyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateBidStrategyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **strategyId** | **string** | Numeric Google Ads bid strategy id. |  |
| **updateBidStrategyRequest** | [**UpdateBidStrategyRequest**](UpdateBidStrategyRequest.md) |  |  |

### Return type

[**UpdateBidStrategy200Response**](UpdateBidStrategy200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bid strategy updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget exhausted; retry later. |  -  |
| **501** | Only available on Google Ads accounts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecampaignadschedule"></a>
# **UpdateCampaignAdSchedule**
> UpdateCampaignAdSchedule200Response UpdateCampaignAdSchedule (string campaignId, UpdateCampaignAdScheduleRequest updateCampaignAdScheduleRequest)

Replace a campaign's ad schedule (dayparting)

Replaces the campaign's whole ad schedule with the windows you send. This is a REPLACE, not a merge: windows you leave out stop serving.  Send `schedule: []` to clear dayparting, which returns the campaign to serving around the clock.  Google rules enforced here, so you get a named field instead of a criterion error: at most 6 windows per day, a window must end after it starts, windows on the same day may not overlap, `endHour` 24 is midnight and cannot carry minutes, and minutes are quarter-hours only (0, 15, 30, 45). `bidModifier` is 0.1-10.0; Google's 0 means \"off\" for devices only, so a window is switched off by leaving it out.  Windows are half-open (Google is exclusive of the end minute), so 09:00-12:00 and 12:00-17:00 on the same day are adjacent and both valid.  Google cannot edit an ad schedule in place (every AdScheduleInfo field is prohibited on update), so this removes the live criteria and creates the new ones in a single atomic mutate. The response is read back from Google and carries the new criterion ids. 

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
    public class UpdateCampaignAdScheduleExample
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
            var updateCampaignAdScheduleRequest = new UpdateCampaignAdScheduleRequest(); // UpdateCampaignAdScheduleRequest | 

            try
            {
                // Replace a campaign's ad schedule (dayparting)
                UpdateCampaignAdSchedule200Response result = apiInstance.UpdateCampaignAdSchedule(campaignId, updateCampaignAdScheduleRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignAdSchedule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCampaignAdScheduleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace a campaign's ad schedule (dayparting)
    ApiResponse<UpdateCampaignAdSchedule200Response> response = apiInstance.UpdateCampaignAdScheduleWithHttpInfo(campaignId, updateCampaignAdScheduleRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignAdScheduleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Numeric Google platform campaign id. |  |
| **updateCampaignAdScheduleRequest** | [**UpdateCampaignAdScheduleRequest**](UpdateCampaignAdScheduleRequest.md) |  |  |

### Return type

[**UpdateCampaignAdSchedule200Response**](UpdateCampaignAdSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The schedule as Google stored it |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access required. Legacy plans need the Ads add-on; included by default on usage-based plans. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **422** | The schedule breaks a Google rule: too many windows on a day, an overlap, a window that ends before it starts, minutes on hour 24, or a bid modifier outside 0.1-10.0. |  -  |
| **501** | Not a Google Ads campaign: ad schedules are a Google criterion. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecampaignassets"></a>
# **UpdateCampaignAssets**
> UpdateCampaignAssets200Response UpdateCampaignAssets (string campaignId, UpdateCampaignAssetsRequest updateCampaignAssetsRequest)

Update campaign assets

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

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
    public class UpdateCampaignAssetsExample
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
            var campaignId = "campaignId_example";  // string | Numeric Google platform id.
            var updateCampaignAssetsRequest = new UpdateCampaignAssetsRequest(); // UpdateCampaignAssetsRequest | 

            try
            {
                // Update campaign assets
                UpdateCampaignAssets200Response result = apiInstance.UpdateCampaignAssets(campaignId, updateCampaignAssetsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCampaignAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update campaign assets
    ApiResponse<UpdateCampaignAssets200Response> response = apiInstance.UpdateCampaignAssetsWithHttpInfo(campaignId, updateCampaignAssetsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignAssetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Numeric Google platform id. |  |
| **updateCampaignAssetsRequest** | [**UpdateCampaignAssetsRequest**](UpdateCampaignAssetsRequest.md) |  |  |

### Return type

[**UpdateCampaignAssets200Response**](UpdateCampaignAssets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Assets returned. |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Ads access is required. |  -  |
| **404** | The account or requested resource was not found or is not accessible. An account ID may have been disconnected and removed. Read GET /v1/accounts for current account IDs. |  -  |
| **409** | The account exists but is inactive or needs reconnection. Reconnect it, then read GET /v1/accounts for its current account ID before retrying. Code: ads_connection_required. |  -  |
| **429** | Google Ads operations budget or platform quota exhausted. |  -  |
| **501** | Only supported on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecampaignconversiongoals"></a>
# **UpdateCampaignConversionGoals**
> UpdateCampaignConversionGoals200Response UpdateCampaignConversionGoals (string campaignId, UpdateCampaignConversionGoalsRequest updateCampaignConversionGoalsRequest)

Update campaign conversion goals

Sets `biddable` on campaign goals, switches `goalConfigLevel`, and/or points the campaign at a custom conversion goal, in one mutate. `customConversionGoalId: null` clears it; Google refuses that (400) while the campaign stays at CAMPAIGN level with no biddable goals, so send `goalConfigLevel: CUSTOMER` with it to fall back to the account goals. Returns the re-read campaign goals.

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
    public class UpdateCampaignConversionGoalsExample
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
            var campaignId = "campaignId_example";  // string | Google campaign id
            var updateCampaignConversionGoalsRequest = new UpdateCampaignConversionGoalsRequest(); // UpdateCampaignConversionGoalsRequest | 

            try
            {
                // Update campaign conversion goals
                UpdateCampaignConversionGoals200Response result = apiInstance.UpdateCampaignConversionGoals(campaignId, updateCampaignConversionGoalsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignConversionGoals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCampaignConversionGoalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update campaign conversion goals
    ApiResponse<UpdateCampaignConversionGoals200Response> response = apiInstance.UpdateCampaignConversionGoalsWithHttpInfo(campaignId, updateCampaignConversionGoalsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignConversionGoalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google campaign id |  |
| **updateCampaignConversionGoalsRequest** | [**UpdateCampaignConversionGoalsRequest**](UpdateCampaignConversionGoalsRequest.md) |  |  |

### Return type

[**UpdateCampaignConversionGoals200Response**](UpdateCampaignConversionGoals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Campaign goals updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Campaign not found |  -  |
| **409** | Campaign matches multiple accessible accounts, or the connection needs reconnecting |  -  |
| **501** | Only available on Google Ads campaigns |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecampaigntargeting"></a>
# **UpdateCampaignTargeting**
> UpdateCampaignTargeting200Response UpdateCampaignTargeting (string campaignId, UpdateCampaignTargetingRequest updateCampaignTargetingRequest)

Edit a Google campaign's device, location, excluded location, or language targeting

Google Ads compliance row M.10: geo and language targeting set at creation must stay editable afterwards. Send at least one of `devices`, `locations`, `excludedLocations`, `languages`, `locationTargetingType`; each provided field REPLACES that field's existing criteria on the campaign (a full set, not a delta). Fields left out of the body are untouched. Google only; every other platform returns 501.  `devices` is the full set of device bid modifiers: a supported device you leave out is switched off with a bid modifier of 0, since Google cannot remove a device criterion. A device the campaign's channel does not carry, and a set that switches every device off, both return 422.  `locations` accepts the same shapes as campaign creation: a bare array of ISO country codes, or an object with `countries`/`regions`/`cities`/`zips`/`metros` key lists (`key` from GET /v1/ads/targeting/search?dimension=geo). Excluded locations are left untouched by `locations`. An empty location list returns 400 instead of removing every criterion: a Google campaign with no location criteria targets every country, so omit `locations` to leave targeting alone.  `excludedLocations` takes the same two shapes and replaces the campaign's negative location criteria (the places it never serves in), leaving the targeted `locations` untouched. An empty list (or `{}`) removes every exclusion. Radius exclusions are not supported. A place cannot be both targeted and excluded: a request whose result would leave one on both sides returns 400 before anything is written, and moving a place from one side to the other in the same request is applied atomically. Example: `{ \"platform\": \"google\", \"targeting\": { \"excludedLocations\": { \"countries\": [\"CA\"], \"regions\": [\"21137\"] } } }`.  The removes and the creates go out in ONE Google `googleAds:mutate`, so a failed edit leaves the campaign's previous set intact rather than a half-applied one.  `languages` is an array of Google's language codes (ISO 639-1, plus variants such as `zh_CN`); an unknown code returns 400.  `locationTargetingType` switches who the location targeting reaches: `presence` (people in or regularly in the locations) or `presence_or_interest` (also people searching for or interested in them). Example: `{ \"platform\": \"google\", \"targeting\": { \"locationTargetingType\": \"presence\" } }`.  The response includes the refreshed `devices`/`locations`/`excludedLocations`/`languages` state read back from Google after the edit, and invalidates the cached copy `GET` on this campaign would otherwise keep serving.  **Demand Gen:** Google keeps a Demand Gen campaign's locations and languages on its ad groups and refuses them on the campaign. When the campaign has one ad group they are written there and the response carries its `adGroupId` (the campaign-level `locations`/`languages` read back then stay empty). With several ad groups the call returns 400 naming them: edit each one with PUT /v1/ads/{adId} `targeting` on an ad of that ad group. Campaigns migrated from Discovery that still target on the campaign keep being written there. `devices` and `locationTargetingType` stay campaign-level. `excludedLocations` is not available on Demand Gen yet and returns 400. 

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
    public class UpdateCampaignTargetingExample
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
            var campaignId = "campaignId_example";  // string | Google platform campaign ID
            var updateCampaignTargetingRequest = new UpdateCampaignTargetingRequest(); // UpdateCampaignTargetingRequest | 

            try
            {
                // Edit a Google campaign's device, location, excluded location, or language targeting
                UpdateCampaignTargeting200Response result = apiInstance.UpdateCampaignTargeting(campaignId, updateCampaignTargetingRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignTargeting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCampaignTargetingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Edit a Google campaign's device, location, excluded location, or language targeting
    ApiResponse<UpdateCampaignTargeting200Response> response = apiInstance.UpdateCampaignTargetingWithHttpInfo(campaignId, updateCampaignTargetingRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateCampaignTargetingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google platform campaign ID |  |
| **updateCampaignTargetingRequest** | [**UpdateCampaignTargetingRequest**](UpdateCampaignTargetingRequest.md) |  |  |

### Return type

[**UpdateCampaignTargeting200Response**](UpdateCampaignTargeting200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Targeting updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **403** | Returned with code &#x60;ads_allowance_exceeded&#x60; when the team has no payment method on file and has reached the 500 free live ads: add a card to resume. |  -  |
| **404** | Campaign not found |  -  |
| **501** | Only available on Google Ads campaigns |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updategoogleassetgroup"></a>
# **UpdateGoogleAssetGroup**
> UpdateGoogleAssetGroup200Response UpdateGoogleAssetGroup (string campaignId, string assetGroupId, UpdateGoogleAssetGroupRequest updateGoogleAssetGroupRequest)

Update a Performance Max asset group

Change the name, status (ENABLED or PAUSED), final URLs or display paths. Only the fields sent are written; null on path1 or path2 clears it. Change assets with the /assets endpoint and product targeting with /listing-group-filters. validateOnly: true validates without writing.

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
    public class UpdateGoogleAssetGroupExample
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
            var campaignId = "campaignId_example";  // string | Google Ads campaign id.
            var assetGroupId = "assetGroupId_example";  // string | Google asset group id.
            var updateGoogleAssetGroupRequest = new UpdateGoogleAssetGroupRequest(); // UpdateGoogleAssetGroupRequest | 

            try
            {
                // Update a Performance Max asset group
                UpdateGoogleAssetGroup200Response result = apiInstance.UpdateGoogleAssetGroup(campaignId, assetGroupId, updateGoogleAssetGroupRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdCampaignsApi.UpdateGoogleAssetGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateGoogleAssetGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a Performance Max asset group
    ApiResponse<UpdateGoogleAssetGroup200Response> response = apiInstance.UpdateGoogleAssetGroupWithHttpInfo(campaignId, assetGroupId, updateGoogleAssetGroupRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdCampaignsApi.UpdateGoogleAssetGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignId** | **string** | Google Ads campaign id. |  |
| **assetGroupId** | **string** | Google asset group id. |  |
| **updateGoogleAssetGroupRequest** | [**UpdateGoogleAssetGroupRequest**](UpdateGoogleAssetGroupRequest.md) |  |  |

### Return type

[**UpdateGoogleAssetGroup200Response**](UpdateGoogleAssetGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated (or validated). |  -  |
| **400** | Invalid request |  -  |
| **401** | Missing or invalid API key. &#x60;code&#x60; is &#x60;missing_credentials&#x60; when no Authorization header was sent and &#x60;invalid_credentials&#x60; when the key is unknown, revoked or expired. |  -  |
| **404** | Resource not found |  -  |
| **422** | Google Ads connection needs reconnecting. |  -  |
| **429** | Google quota or the Zernio Google operations burst limit is exhausted. |  -  |
| **501** | Campaign is not on Google Ads. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

