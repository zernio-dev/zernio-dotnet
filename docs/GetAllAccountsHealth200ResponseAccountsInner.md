# Zernio.Model.GetAllAccountsHealth200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Username** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**CanPost** | **bool** |  | [optional] 
**CanFetchAnalytics** | **bool** |  | [optional] 
**TokenValid** | **bool** |  | [optional] 
**TokenExpiresAt** | **DateTime** |  | [optional] 
**NeedsReconnect** | **bool** | True when the token is expired or revoked, permissions are missing, the account is inactive, or the platform rejected its stored credentials (the same flag the account listing reports as needsReconnection). | [optional] 
**Issues** | **List&lt;string&gt;** |  | [optional] 
**MessagingRestriction** | [**GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction**](GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

