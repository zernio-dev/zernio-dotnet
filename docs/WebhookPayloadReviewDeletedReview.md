# Zernio.Model.WebhookPayloadReviewDeletedReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Google: full review name. Facebook: the review id from review.new. | 
**Platform** | **string** |  | 
**Rating** | **int?** | Star rating the reviewer gave. Null when it was never recorded. | 
**CreatedAt** | **DateTime?** | When the reviewer posted the review. Null when it was never recorded. Always null on Facebook. | 
**LastSeenAt** | **DateTime** | Last time Zernio saw Google return this review. On Facebook, when Meta&#39;s removal notice arrived. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

