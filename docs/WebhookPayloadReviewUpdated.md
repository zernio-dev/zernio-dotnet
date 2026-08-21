# Zernio.Model.WebhookPayloadReviewUpdated
Webhook payload for the review.updated event. Fired when the reviewer edits their text or rating, or when a reply is added (via the API or directly on the platform). Same shape as review.new. When a reply is present, review.hasReply is true and review.reply is populated. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Review** | [**ReviewWebhookReview**](ReviewWebhookReview.md) |  | 
**Account** | [**WebhookPayloadReviewNewAccount**](WebhookPayloadReviewNewAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

