# Zernio.Model.WebhookPayloadMessageSentMetadataLocation
WhatsApp only. The location pin this message carries, in the same shape the inbox send API accepts. Present on API sends that passed `location`, and on Coexistence echoes of a pin shared from the WhatsApp Business app. The message `text` is only the emoji preview (`📍 <name>`); the pin itself lives here. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Latitude** | **decimal** | Latitude in decimal degrees. | [optional] 
**Longitude** | **decimal** | Longitude in decimal degrees. | [optional] 
**Name** | **string** | Location name, when one was given. | [optional] 
**Address** | **string** | Street address, when one was given. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

