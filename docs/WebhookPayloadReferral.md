# Zernio.Model.WebhookPayloadReferral
Webhook payload for referral received events (Instagram, Facebook Messenger)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Referral** | [**WebhookPayloadReferralReferral**](WebhookPayloadReferralReferral.md) |  | 
**Sender** | [**WebhookPayloadReferralSender**](WebhookPayloadReferralSender.md) |  | 
**Conversation** | [**InboxWebhookConversation**](InboxWebhookConversation.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

