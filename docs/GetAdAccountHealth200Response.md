# Zernio.Model.GetAdAccountHealth200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Ready** | **bool** | False when a create or boost on this ad account would be refused; &#x60;blockers&#x60; says why. | [optional] 
**Blockers** | [**List&lt;GetAdAccountHealth200ResponseBlockersInner&gt;**](GetAdAccountHealth200ResponseBlockersInner.md) |  | [optional] 
**CheckedAt** | **DateTime** |  | [optional] 
**Checks** | [**List&lt;GetAdAccountHealth200ResponseChecksInner&gt;**](GetAdAccountHealth200ResponseChecksInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

