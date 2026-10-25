# Zernio.Model.ListTikTokSmartPlusReviews200ResponseItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SmartPlusAdId** | **string** |  | [optional] 
**AdGroupId** | **string** |  | [optional] 
**CampaignId** | **string** |  | [optional] 
**Review** | [**TikTokSmartPlusAdLevelReview**](TikTokSmartPlusAdLevelReview.md) |  | [optional] 
**Materials** | [**List&lt;TikTokSmartPlusMaterialReview&gt;**](TikTokSmartPlusMaterialReview.md) | One entry per creative TikTok reviewed (&#x60;material_review_infos&#x60;). | [optional] 
**ReadAt** | **DateTime** | When the verdict was read from TikTok, kept as is when served from the store. Older than &#x60;maxAgeSeconds&#x60; means stale. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

