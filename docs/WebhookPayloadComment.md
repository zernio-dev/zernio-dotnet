# Zernio.Model.WebhookPayloadComment
Webhook payload for comment received events (Instagram, Facebook, Threads, YouTube, LinkedIn, Bluesky, Reddit, TikTok). X/Twitter does NOT fire this event. TikTok events carry only the author id: the comment.update webhook has no username, picture or owner flag.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Comment** | [**WebhookPayloadCommentComment**](WebhookPayloadCommentComment.md) |  | 
**Post** | [**WebhookPayloadCommentPost**](WebhookPayloadCommentPost.md) |  | 
**Account** | [**WebhookPayloadCommentAccount**](WebhookPayloadCommentAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

