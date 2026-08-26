# Zernio.Model.WebhookPayloadMessageDeleted
Webhook payload for message.deleted events. Fires when the sender deletes (unsends) a message. Supported platforms: Instagram (incoming unsend) and WhatsApp, in both directions: an outgoing message the business deleted (via the Cloud API, or from the WhatsApp Business app on a Coexistence number) and an incoming message the customer deleted. Read `message.direction` to tell the two apart.  The message.text and message.attachments fields retain the content that existed before the delete. The Zernio dashboard UI does not show this content, but authorized API consumers may access it for moderation, compliance, or archival use cases. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Event** | **string** |  | 
**Message** | [**InboxWebhookMessage**](InboxWebhookMessage.md) |  | 
**DeletedAt** | **DateTime** |  | 
**Conversation** | [**InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

