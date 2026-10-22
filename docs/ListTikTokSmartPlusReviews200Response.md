# Zernio.Model.ListTikTokSmartPlusReviews200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** |  | [optional] 
**IncludeDeleted** | **bool** |  | [optional] 
**Page** | **int** |  | [optional] 
**PageSize** | **int** |  | [optional] 
**TotalPages** | **int** |  | [optional] 
**TotalSmartPlusAds** | **int** | Smart+ ads of the advertiser across all pages. | [optional] 
**Items** | [**List&lt;ListTikTokSmartPlusReviews200ResponseItemsInner&gt;**](ListTikTokSmartPlusReviews200ResponseItemsInner.md) |  | [optional] 
**FailedSmartPlusAds** | [**List&lt;ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner&gt;**](ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner.md) | Smart+ ads of this page whose review TikTok refused on its own (for example an ad deleted on TikTok since the listing was cached). Zernio splits a refused batch in halves (at most 16 extra calls per page), so the other ads of the batch are still read; ads left unresolved by that cap carry the batch error. Empty when none. | [optional] 
**Incomplete** | **bool** | True when some Smart+ ads of this page could not be read because of TikTok&#39;s review quota. | [optional] 
**PendingSmartPlusAdIds** | **List&lt;string&gt;** | Smart+ ads of this page still to read. Empty when complete. | [optional] 
**RetryAfterSeconds** | **int?** | Seconds to wait before reading this page again. Null when complete. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

