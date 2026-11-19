# Zernio.Model.GetAdReview200ResponseReviewAssetGroup
Google Performance Max only. The asset group's serving status and each linked asset's policy review.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PrimaryStatus** | **string** | asset_group.primary_status, verbatim: ELIGIBLE, LIMITED, NOT_ELIGIBLE, PAUSED, PENDING, REMOVED. | 
**PrimaryStatusReasons** | **List&lt;string&gt;** | asset_group.primary_status_reasons, verbatim, such as ASSET_GROUP_DISAPPROVED, ASSET_GROUP_UNDER_REVIEW, ASSET_GROUP_LIMITED, CAMPAIGN_PAUSED. Empty when the group serves without issues. | 
**Assets** | [**List&lt;GetAdReview200ResponseReviewAssetGroupAssetsInner&gt;**](GetAdReview200ResponseReviewAssetGroupAssetsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

