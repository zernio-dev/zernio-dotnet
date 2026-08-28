# Zernio.Model.CreateInboxConversationRequestHeaderLocation
WhatsApp only. Required to send a template whose approved header format is LOCATION: Meta only accepts the location's lat/long at send time, never at template creation, so there is nothing to fill in automatically. Cannot be combined with headerMedia (a template has exactly one header).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Latitude** | **decimal** | Latitude in decimal degrees. | 
**Longitude** | **decimal** | Longitude in decimal degrees. | 
**Name** | **string** | Location name shown to the recipient (e.g. a business name). | [optional] 
**Address** | **string** | Location address shown to the recipient. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

