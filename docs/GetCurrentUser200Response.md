# Zernio.Model.GetCurrentUser200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Email** | **string** | Only returned to a dashboard session. Omitted for API keys. | [optional] 
**Image** | **string** |  | [optional] 
**Role** | **string** | One of owner, admin, billing_admin, member or viewer. Always owner when isRoot is true. | [optional] 
**IsRoot** | **bool** | True when the user owns the account, false when they were invited to it. | [optional] 
**InvitedBy** | **string** | Id of the user who invited this user. Null when isRoot is true. | [optional] 
**InvitedToProfile** | **string** | Only present when isRoot is false. | [optional] 
**InvitedToProfiles** | **List&lt;string&gt;** | Ids of the profiles an invited user is limited to. Empty means every profile. Only present when isRoot is false. | [optional] 
**DisabledResourceGroups** | **List&lt;string&gt;** | Resource groups turned off for an invited user. Null or empty means none. Only present when isRoot is false. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**LastLoginAt** | **DateTime?** | Last sign-in, stamped at most once an hour. Null when no sign-in has been recorded. | [optional] 
**WorkspaceId** | **string** | Id of the workspace the credential acts in. Null when the user has no workspace yet. | [optional] 
**WorkspaceName** | **string** | Name of that workspace. Null when workspaceId is null. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

