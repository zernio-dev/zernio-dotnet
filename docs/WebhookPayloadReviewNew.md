# Zernio.Model.WebhookPayloadReviewNew
Webhook payload for the review.new event (new review posted on a connected account).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Review** | [**ReviewWebhookReview**](ReviewWebhookReview.md) |  | 
**Account** | [**WebhookPayloadReviewNewAccount**](WebhookPayloadReviewNewAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

