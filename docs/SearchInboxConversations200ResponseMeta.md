# Zernio.Model.SearchInboxConversations200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountsQueried** | **int** |  | [optional] 
**AccountsFailed** | **int** |  | [optional] 
**FailedAccounts** | [**List&lt;SearchInboxConversations200ResponseMetaFailedAccountsInner&gt;**](SearchInboxConversations200ResponseMetaFailedAccountsInner.md) |  | [optional] 
**LastUpdated** | **DateTime** |  | [optional] 
**ContentNotRetained** | **bool** | True when a searched account belongs to a team that does not retain content. Message text is not searchable there, only identifiers match. | [optional] 
**AccountsSkipped** | [**List&lt;ListInboxConversations200ResponseMetaAccountsSkippedInner&gt;**](ListInboxConversations200ResponseMetaAccountsSkippedInner.md) | Connected messaging accounts that cannot be searched (live-fetched platforms) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

