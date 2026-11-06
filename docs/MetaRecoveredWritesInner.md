# Zernio.Model.MetaRecoveredWritesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Id** | **string** | The Meta object id this response uses. | 
**Adopted** | **bool** | Always true when present. Zernio found this object by name under its parent and reused it instead of creating it again. | [optional] 
**RepostedAfter** | **string** | Zernio sent the create again after Meta answered a 5xx and the read-back found no such object. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

