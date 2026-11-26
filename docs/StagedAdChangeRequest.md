# Zernio.Model.StagedAdChangeRequest
Only with type `operation`: the write that was staged as its request. Confirm sends this request through its own route.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Operation** | **string** | The operationId of the staged write. Every write in this list accepts &#x60;stage: true&#x60; in its body, or &#x60;?stage&#x3D;true&#x60; when it has no body. | 
**Method** | **string** |  | 
**Path** | **string** | The path of the write, for example /v1/ads/keywords. | 
**Params** | **Dictionary&lt;string, string&gt;** | The path values of the staged request, by the names in &#x60;path&#x60;. | [optional] 
**Query** | **Dictionary&lt;string, string&gt;** | The query values of the staged request, without &#x60;stage&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

