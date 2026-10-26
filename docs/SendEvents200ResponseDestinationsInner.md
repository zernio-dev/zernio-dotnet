# Zernio.Model.SendEvents200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**DestinationId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**EventsSent** | **int** | Events the platform accepted. | [optional] 
**EventsFailed** | **int** |  | [optional] 
**Failures** | [**List&lt;SendEvents200ResponseDestinationsInnerFailuresInner&gt;**](SendEvents200ResponseDestinationsInnerFailuresInner.md) |  | [optional] 
**Error** | **string** | Set when the destination could not be reached at all (account disconnected, unsupported platform, platform error). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

