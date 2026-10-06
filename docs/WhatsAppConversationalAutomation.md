# Zernio.Model.WhatsAppConversationalAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EnableWelcomeMessage** | **bool** | When true, Meta sends a &#x60;request_welcome&#x60; event the first time a person opens a chat with the number. | [optional] 
**Prompts** | **List&lt;string&gt;** | Ice breakers shown to a person opening a chat. Tapping one sends its text as a normal message. | [optional] 
**Commands** | [**List&lt;WhatsAppConversationalAutomationCommandsInner&gt;**](WhatsAppConversationalAutomationCommandsInner.md) | Slash commands shown when a person types &#x60;/&#x60;. Names are unique, letters, digits and underscores, without the slash. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

