# Zernio.Model.CreateGoogleOrgConnectionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**Domain** | **string** | The Workspace domain the admin delegates. | 
**Scopes** | **List&lt;CreateGoogleOrgConnectionRequest.ScopesEnum&gt;** | Areas the mailboxes get, the same as a user connect. | 
**AdminEmail** | **string** | A super admin, used to list the domain&#39;s users. | [optional] 
**AllowedEmails** | **List&lt;string&gt;** | Addresses or &#x60;@domain&#x60; entries mailboxes must match. Omit for every mailbox. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

