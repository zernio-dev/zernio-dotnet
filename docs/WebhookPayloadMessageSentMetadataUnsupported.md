# Zernio.Model.WebhookPayloadMessageSentMetadataUnsupported
WhatsApp only. Meta's own reason this message has no renderable body. Present on Coexistence echoes of a message sent from the WhatsApp Business app that Meta could not render (for example an album, code 131051: message type currently not supported). Absent otherwise. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int** | Meta&#39;s numeric error code (e.g. 131051). | [optional] 
**Title** | **string** | Meta&#39;s short error title. | [optional] 
**Details** | **string** | Meta&#39;s human-readable error detail string. | [optional] 
**Type** | **string** | Meta&#39;s name for the content WhatsApp could not deliver, e.g. unknown or album. Absent when Meta sends none. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

