# Zernio.Model.WebhookPayloadMessageMetadataLocation
WhatsApp only. The location pin the user shared, forwarded verbatim from Meta. The message `text` is only the emoji preview (`📍 <name>`); the coordinates live here. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Latitude** | **decimal** | Latitude in decimal degrees. | [optional] 
**Longitude** | **decimal** | Longitude in decimal degrees. | [optional] 
**Name** | **string** | Location name, when the user shared a named place. | [optional] 
**Address** | **string** | Street address, when Meta sends one. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

