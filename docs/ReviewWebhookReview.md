# Zernio.Model.ReviewWebhookReview
Review data shared by review.new, review.updated and review.restored payloads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform review ID (e.g. \&quot;accounts/123/locations/456/reviews/789\&quot; for Google Business Profile). | 
**Platform** | **string** | Platform the review originated on (Google Business Profile or Facebook Pages). | 
**Rating** | **int?** | Star rating the reviewer gave. Null for a Facebook recommendation without stars. | 
**RecommendationType** | **string** | Facebook only. Whether the reviewer recommended the Page. | [optional] 
**Text** | **string** | Review text content. May be empty if the reviewer left only a rating. | 
**Reviewer** | [**ReviewWebhookReviewReviewer**](ReviewWebhookReviewReviewer.md) |  | 
**CreatedAt** | **DateTime** |  | 
**HasReply** | **bool** | Whether the connected account has replied to this review. | 
**Reply** | [**ReviewWebhookReviewReply**](ReviewWebhookReviewReply.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

