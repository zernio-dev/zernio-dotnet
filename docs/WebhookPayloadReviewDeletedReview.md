# Zernio.Model.WebhookPayloadReviewDeletedReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Full review name, matching review.id on the review.new event (\&quot;accounts/123/locations/456/reviews/789\&quot;). | 
**Platform** | **string** |  | 
**Rating** | **int?** | Star rating the reviewer gave. Null when it was never recorded. | 
**CreatedAt** | **DateTime?** | When the reviewer posted the review. Null when it was never recorded. | 
**LastSeenAt** | **DateTime** | Last time Zernio saw Google return this review. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

