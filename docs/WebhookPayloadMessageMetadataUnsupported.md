# Zernio.Model.WebhookPayloadMessageMetadataUnsupported
WhatsApp only. Meta's own reason this message has no renderable body. Present when Meta attached an error to the inbound payload; in practice the `unsupported`, `errors` and `unknown` types (code 131051: message type currently not supported). `text` on those messages is the fixed `[Unsupported message]` placeholder. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int** | Meta&#39;s numeric error code (e.g. 131051). | [optional] 
**Title** | **string** | Meta&#39;s short error title. | [optional] 
**Details** | **string** | Meta&#39;s human-readable error detail string. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

