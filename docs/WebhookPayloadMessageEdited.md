# Zernio.Model.WebhookPayloadMessageEdited
Webhook payload for message.edited events. Fires when the sender edits a previously-sent message. Supported platforms: Instagram, Facebook Messenger, Telegram, WhatsApp. The message object reflects the LATEST state; editHistory contains every prior version in order (oldest first), so the last entry is the version immediately before the current content. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Event** | **string** |  | 
**Message** | [**InboxWebhookMessage**](InboxWebhookMessage.md) |  | 
**EditHistory** | [**List&lt;InboxMessageEditHistoryEntry&gt;**](InboxMessageEditHistoryEntry.md) | Prior versions of the message, oldest first. | 
**EditCount** | **int** | Total number of edits applied to this message. | 
**EditedAt** | **DateTime** | When the most recent edit happened. | 
**Conversation** | [**InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

