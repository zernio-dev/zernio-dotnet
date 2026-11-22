# Zernio.Model.CreateWorkspaceRequestApiKey
Mint a key that acts in the new workspace. The response then carries it in `apiKey`, with its full value shown only once.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Permission** | **string** |  | [optional] [default to PermissionEnum.ReadWrite]
**ExpiresIn** | **int** | Days until expiry. | [optional] 
**DisabledResourceGroups** | **List&lt;CreateWorkspaceRequestApiKey.DisabledResourceGroupsEnum&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

