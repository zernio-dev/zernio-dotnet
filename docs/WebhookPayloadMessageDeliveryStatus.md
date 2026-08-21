# Zernio.Model.WebhookPayloadMessageDeliveryStatus
Shared payload for message.delivered, message.read, and message.failed events. Fires when the platform reports a new delivery state for an outgoing message.  Platform support:   * message.delivered: WhatsApp, Facebook Messenger, SMS.   * message.read: WhatsApp, Facebook Messenger, Instagram. Not SMS     (carriers report delivery, never read).   * message.failed: WhatsApp and SMS (other platforms don't expose     per-message failure via webhook). On SMS, `error.code` is the     carrier's numeric code and `error.message` its reason. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Event** | **string** |  | 
**Message** | [**InboxWebhookMessage**](InboxWebhookMessage.md) |  | 
**StatusAt** | **DateTime** | When the platform reported this status. | 
**Error** | [**WebhookPayloadMessageDeliveryStatusError**](WebhookPayloadMessageDeliveryStatusError.md) |  | [optional] 
**Conversation** | [**InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

