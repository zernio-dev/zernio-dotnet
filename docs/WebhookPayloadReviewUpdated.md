# Zernio.Model.WebhookPayloadReviewUpdated
Webhook payload for the `review.updated` event. Fired when the reviewer edits their text or rating, or when a reply is added (via the API or directly on the platform). Same shape as `review.new`; when a reply is present `review.hasReply` is `true` and `review.reply` is populated. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Review** | [**ReviewWebhookReview**](ReviewWebhookReview.md) |  | 
**Account** | [**WebhookPayloadReviewNewAccount**](WebhookPayloadReviewNewAccount.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

