# Zernio.Model.WebhookPayloadCallReceived
Webhook payload for the `call.received` event. Fires for both inbound (UIC) and outbound (BIC) calls; branch on `call.direction` to tell them apart. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Call** | [**WebhookPayloadCallReceivedCall**](WebhookPayloadCallReceivedCall.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

