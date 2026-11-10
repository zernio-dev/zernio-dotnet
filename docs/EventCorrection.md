# Zernio.Model.EventCorrection
What happened to a correction at one destination the event was forwarded to.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**DestinationId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Status** | **string** | &#x60;corrected&#x60;: the platform changed its count. &#x60;not_supported&#x60;: the platform has no API to change a conversion it already counted. &#x60;failed&#x60;: see &#x60;error&#x60;. | [optional] 
**Error** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

