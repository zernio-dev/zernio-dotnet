# Zernio.Model.MetaPagePartner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BusinessId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**PermittedTasks** | **List&lt;string&gt;** | Tasks the partner holds, in the bare spelling the grant takes (ADVERTISE, ANALYZE, MANAGE, ...). Meta reads them back with a PROFILE_PLUS_ prefix, which is stripped here; partners granted in Business Settings may hold tasks beyond the six the grant accepts, such as MANAGE_LEADS or REVENUE. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

