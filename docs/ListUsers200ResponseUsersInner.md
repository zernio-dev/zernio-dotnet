# Zernio.Model.ListUsers200ResponseUsersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Email** | **string** |  | [optional] 
**Role** | **string** |  | [optional] 
**IsRoot** | **bool** |  | [optional] 
**ProfileAccess** | **List&lt;string&gt;** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**LastLoginAt** | **DateTime** | Last sign-in, stamped at most once an hour, so it is accurate to within an hour rather than to the exact session. Omitted for members with no recorded sign-in since the field shipped, which does not mean they never signed in. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

