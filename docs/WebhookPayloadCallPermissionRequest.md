# Zernio.Model.WebhookPayloadCallPermissionRequest
Webhook payload for the `call.permission_request` event. Fires when a consumer accepts or rejects an interactive `call_permission_request` message. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Event** | **string** |  | 
**Permission** | [**WebhookPayloadCallPermissionRequestPermission**](WebhookPayloadCallPermissionRequestPermission.md) |  | 
**Account** | [**InboxWebhookAccount**](InboxWebhookAccount.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

