# Zernio.Model.WebhookPayloadNotificationSentNotification

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Category** | **string** | The email notification preference this notification belongs to. | 
**Type** | **string** |  | 
**Subject** | **string** | The email subject. | 
**Text** | **string** | The email body as plain text, without the greeting. | 
**Url** | **string** | Dashboard link for the notification. | 
**Refs** | [**WebhookPayloadNotificationSentNotificationRefs**](WebhookPayloadNotificationSentNotificationRefs.md) |  | 
**Reason** | **string** | Why the account was disconnected. Only on account_disconnected. | [optional] 
**Actions** | [**List&lt;WebhookPayloadNotificationSentNotificationActionsInner&gt;**](WebhookPayloadNotificationSentNotificationActionsInner.md) | API calls that act on the notification, with the ids already in the path. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

