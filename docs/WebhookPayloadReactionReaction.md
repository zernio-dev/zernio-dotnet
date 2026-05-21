# Zernio.Model.WebhookPayloadReactionReaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Emoji** | **string** | The emoji reacted with. May be an empty string when &#x60;action&#x60; is &#x60;removed&#x60; on WhatsApp (Meta does not report which emoji was removed).  | 
**Action** | **string** |  | 
**MessageId** | **string** | Internal Zernio message ID of the reacted-to message, when resolvable from the platform ID. | [optional] 
**PlatformMessageId** | **string** | Platform-native ID of the reacted-to message (e.g. WhatsApp wamid). | 
**Sender** | [**WebhookPayloadReactionReactionSender**](WebhookPayloadReactionReactionSender.md) |  | 
**ReactedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

