# Zernio.Model.UpdateAd200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ValidateOnly** | **bool** | Present and true when the request was sent with validateOnly: nothing was changed. The other fields of a real update are then absent. | [optional] 
**Results** | [**List&lt;AdWriteValidationResult&gt;**](AdWriteValidationResult.md) | validateOnly only: one entry, the object Meta validated. | [optional] 
**Ad** | [**Ad**](Ad.md) |  | [optional] 
**Message** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

