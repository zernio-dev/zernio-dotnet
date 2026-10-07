# Zernio.Model.GetAdReview200ResponseReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Approved** | **bool?** | TikTok &#x60;is_approved&#x60;. | [optional] 
**ReviewStatus** | **string** | TikTok &#x60;review_status&#x60;, verbatim: ALL_AVAILABLE (approved everywhere), PART_AVAILABLE (approved for part of the targeting), UNAVAILABLE (rejected). | [optional] 
**ForbiddenPlacements** | **List&lt;string&gt;** |  | [optional] 
**ForbiddenAges** | **List&lt;string&gt;** |  | [optional] 
**ForbiddenLocations** | **List&lt;string&gt;** |  | [optional] 
**ForbiddenOperatingSystems** | **List&lt;string&gt;** |  | [optional] 
**Rejections** | [**List&lt;GetAdReview200ResponseReviewRejectionsInner&gt;**](GetAdReview200ResponseReviewRejectionsInner.md) | One entry per rejected piece of content (TikTok &#x60;reject_info&#x60;). Empty when the ad was approved. | [optional] 
**ApprovalStatus** | **string** | Google only. ad_group_ad.policy_summary.approval_status, verbatim. | [optional] 
**PolicyTopics** | [**List&lt;GetAdReview200ResponseReviewPolicyTopicsInner&gt;**](GetAdReview200ResponseReviewPolicyTopicsInner.md) | Google only. ad_group_ad.policy_summary.policy_topic_entries. | [optional] 
**ReadAt** | **DateTime** | When the verdict was read from the platform. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

