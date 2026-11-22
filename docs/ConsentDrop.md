# Zernio.Model.ConsentDrop
An event the destination did not get because the visitor did not consent.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventIndex** | **int** | Index into the events sent to this destination. | [optional] 
**EventId** | **string** |  | [optional] 
**Reason** | **string** | &#x60;consent_denied&#x60;: a signal the platform needs is &#x60;DENIED&#x60;. &#x60;consent_missing&#x60;: the visitor is in the EEA, UK or CH and the signal was never given. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

