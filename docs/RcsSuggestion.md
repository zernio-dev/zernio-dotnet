# Zernio.Model.RcsSuggestion
A tappable chip. Labels are max 25 characters. postbackData (max 2048) comes back unchanged in message.received metadata as postbackPayload when tapped; defaults to the label. Any string works, JSON included: values outside A-Z a-z 0-9 - _ . are encoded on the wire and decoded for you.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Text** | **string** |  | 
**PostbackData** | **string** |  | [optional] 
**PhoneNumber** | **string** | E.164 | 
**Url** | **string** |  | 
**Application** | **string** |  | [optional] [default to ApplicationEnum.BROWSER]
**WebviewViewMode** | **string** |  | [optional] [default to WebviewViewModeEnum.FULL]
**Latitude** | **decimal** |  | [optional] 
**Longitude** | **decimal** |  | [optional] 
**Query** | **string** |  | [optional] 
**Label** | **string** |  | [optional] 
**StartTime** | **DateTime** |  | 
**EndTime** | **DateTime** |  | 
**Title** | **string** |  | 
**Description** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

