# Zernio.Model.OnWhatsAppAutomaticEventRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Event** | **string** |  | [optional] 
**Timestamp** | **DateTime** |  | [optional] 
**AccountId** | **string** | SocialAccount id of the WhatsApp number whose conversation was flagged. | [optional] 
**ConversationId** | **string** | Zernio conversation id, when the thread could be resolved. | [optional] 
**PlatformMessageId** | **string** | The wamid of the message Meta&#39;s analysis flagged. | [optional] 
**EventName** | **string** | Meta-detected event: &#x60;LeadSubmitted&#x60; | &#x60;Purchase&#x60;. | [optional] 
**CtwaClid** | **string** | Meta&#39;s CTWA click id, the Conversions API match key. | [optional] 
**CustomData** | [**OnWhatsAppAutomaticEventRequestCustomData**](OnWhatsAppAutomaticEventRequestCustomData.md) |  | [optional] 
**DetectedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

