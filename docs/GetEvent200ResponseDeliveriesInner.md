# Zernio.Model.GetEvent200ResponseDeliveriesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**DestinationId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Status** | **string** | &#x60;dropped&#x60;: not sent because the visitor did not consent; &#x60;errorCode&#x60; says why (&#x60;consent_denied&#x60; or &#x60;consent_missing&#x60;). | [optional] 
**Attempt** | **int** | Send attempt (1 &#x3D; the first). | [optional] 
**Error** | **string** |  | [optional] 
**ErrorCode** | **string** |  | [optional] 
**SentAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

