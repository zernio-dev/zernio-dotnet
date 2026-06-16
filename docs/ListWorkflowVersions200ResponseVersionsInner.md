# Zernio.Model.ListWorkflowVersions200ResponseVersionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**VarVersion** | **int** | Monotonically increasing version number | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**CreatedBy** | **string** | User id that authored this version | [optional] 
**CreatedByEmail** | **string** | Denormalized email so the history UI can render without a join | [optional] 
**RestoredFromVersion** | **int** | When non-null, this snapshot was created by restoring that version | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

