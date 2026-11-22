# Zernio.Model.WebhookPayloadMessageMetadataLocation
WhatsApp and iMessage. The location pin the user shared. On WhatsApp it is forwarded verbatim from Meta and the message `text` is only the emoji preview (`📍 <name>`); the coordinates live here. On iMessage it is parsed from a Maps link in `text`, which stays as sent. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Latitude** | **decimal** | Latitude in decimal degrees. | [optional] 
**Longitude** | **decimal** | Longitude in decimal degrees. | [optional] 
**Name** | **string** | Location name, when the user shared a named place. | [optional] 
**Address** | **string** | Street address, when Meta sends one. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

