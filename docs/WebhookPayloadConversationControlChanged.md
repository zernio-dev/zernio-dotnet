# Zernio.Model.WebhookPayloadConversationControlChanged
WhatsApp only. Who answers a conversation changed: Meta Business Agent took it over, handed it to you, or another partner app took it. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Conversation** | [**WebhookPayloadConversationStartedConversation**](WebhookPayloadConversationStartedConversation.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Control** | [**WebhookPayloadConversationControlChangedControl**](WebhookPayloadConversationControlChangedControl.md) |  | 
**ChangedAt** | **DateTime** |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

