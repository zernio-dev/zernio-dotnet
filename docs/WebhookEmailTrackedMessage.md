# Zernio.Model.WebhookEmailTrackedMessage
The tracked message an email.* event is about. `messageId` and `threadId` are the provider ids (read the message with `GET /v1/email/messages/{messageId}`); `metadata` is what you sent with it.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** |  | [optional] 
**ThreadId** | **string** |  | [optional] 
**TrackingId** | **string** | Also returned as &#x60;data.trackingId&#x60; by the send. | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

