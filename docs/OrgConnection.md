# Zernio.Model.OrgConnection
A Google Workspace domain or Microsoft 365 tenant whose administrator granted Zernio access to its mailboxes once.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Provider** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**Areas** | **List&lt;OrgConnection.AreasEnum&gt;** |  | [optional] 
**Domain** | **string** |  | [optional] 
**TenantId** | **string** |  | [optional] 
**AdminEmail** | **string** |  | [optional] 
**AllowedEmails** | **List&lt;string&gt;** |  | [optional] 
**LastError** | **string** |  | [optional] 
**VerifiedAt** | **DateTime?** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**Setup** | [**OrgConnectionSetup**](OrgConnectionSetup.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

