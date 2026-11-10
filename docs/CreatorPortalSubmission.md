# Zernio.Model.CreatorPortalSubmission

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Platform** | **string** |  | 
**PostId** | **string** |  | 
**HasSparkCode** | **bool** | A TikTok post whose Spark code the creator pasted, so the brand can run it as a Spark Ad. The code itself is never returned. | 
**Url** | **string** |  | 
**Status** | **string** |  | 
**SubmittedAt** | **DateTime** |  | 
**PublishedAt** | **DateTime?** |  | 
**Views** | **int** | Latest view count read for the post. | 
**Engagements** | **int?** | The campaign engagement types summed at the latest read. Null until the post is read. | 
**ViewsFromAds** | **int?** | Views that came from ads the creator ran, on YouTube and X. Null where the platform does not report them or before the first read. | 
**EarnedCents** | **int** |  | 
**RejectReason** | **string** |  | 
**Flags** | **List&lt;CreatorPortalSubmission.FlagsEnum&gt;** | Creator-safe flags only. Every other review flag shows as &#x60;under_review&#x60;. | 
**TrackingEndsAt** | **DateTime?** |  | 
**DraftId** | **string** | The approved draft this post publishes. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

