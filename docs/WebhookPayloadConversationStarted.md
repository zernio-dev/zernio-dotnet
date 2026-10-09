# Zernio.Model.WebhookPayloadConversationStarted
Fired once when a new conversation begins, in either direction. A conversation starts the first time an account and a contact exchange a message on any DM platform (Instagram, Messenger/Facebook, Telegram, WhatsApp, X, Reddit, Bluesky, SMS, TikTok). Platform-agnostic: one subscription covers every DM platform. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Event** | **string** |  | 
**Conversation** | [**InboxWebhookConversationDetail**](InboxWebhookConversationDetail.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**StartedAt** | **DateTime** | When the conversation document was created. | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

