# Zernio.Model.WebhookPayloadMessageDeliveryStatus
Shared payload for message.delivered, message.read, message.played and message.failed events. Fires when the platform reports a new delivery state for an outgoing message.  Platform support:   * message.delivered: WhatsApp, Facebook Messenger, SMS, RCS.   * message.read: WhatsApp, Facebook Messenger, Instagram, RCS. Not SMS     (carriers report delivery, never read).   * message.played: WhatsApp only, voice messages.   * message.failed: WhatsApp, SMS and RCS (other platforms don't expose     per-message failure via webhook). On SMS, `error.code` is the     carrier's numeric code and `error.message` its reason. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Event** | **string** |  | 
**Message** | [**InboxWebhookMessage**](InboxWebhookMessage.md) |  | 
**StatusAt** | **DateTime** | When the platform reported this status. | 
**Error** | [**WebhookPayloadMessageDeliveryStatusError**](WebhookPayloadMessageDeliveryStatusError.md) |  | [optional] 
**Pricing** | [**WhatsAppMessagePricing**](WhatsAppMessagePricing.md) |  | [optional] 
**BillingConversation** | [**WhatsAppBillingConversation**](WhatsAppBillingConversation.md) |  | [optional] 
**Conversation** | [**InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

