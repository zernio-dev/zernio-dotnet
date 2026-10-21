# Zernio.Model.GetTikTokSmartPlusAdReview200ResponseReview
The ad-level verdict (`smart_plus_ad_review_infos`). Null when TikTok returned none.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ReviewStatus** | **TikTokSmartPlusReviewStatus** |  | [optional] 
**RawReviewStatus** | **string** | TikTok &#x60;review_status&#x60;, verbatim. | [optional] 
**RejectReasons** | **List&lt;string&gt;** | Every distinct reason across &#x60;rejections&#x60;. | [optional] 
**PassedLocations** | **List&lt;string&gt;** | Location codes that passed the review. | [optional] 
**AppealStatus** | **string** | TikTok &#x60;appeal_status&#x60;, verbatim: NOT_APPEALED, APPEALING, APPEAL_SUCCESSFUL, APPEAL_FAILED, APPEAL_DONE. | [optional] 
**AppealRejectReasons** | **List&lt;string&gt;** |  | [optional] 
**Rejections** | [**List&lt;TikTokReviewRejection&gt;**](TikTokReviewRejection.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

