# Zernio.Model.CreateWorkspaceApiKeyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Permission** | **string** | &#39;read&#39; restricts the key to GET requests. | [optional] [default to PermissionEnum.ReadWrite]
**ExpiresIn** | **int** | Days until expiry. Omit for a key that never expires. | [optional] 
**DisabledResourceGroups** | **List&lt;CreateWorkspaceApiKeyRequest.DisabledResourceGroupsEnum&gt;** | Resource groups the key cannot use, as on &#x60;POST /v1/api-keys&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

