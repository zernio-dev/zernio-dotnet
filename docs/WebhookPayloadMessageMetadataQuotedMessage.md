# Zernio.Model.WebhookPayloadMessageMetadataQuotedMessage
Zernio's own ids for the message this one quote-replies to. Present only when that message is stored; WhatsApp only today.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** | Internal id of the stored quoted message. | [optional] 
**PlatformMessageId** | **string** | The STORED message&#39;s platform id (what message.sent and list-messages return). Can differ from quotedMessageId, because Meta renders one message under a different wamid per perspective. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

