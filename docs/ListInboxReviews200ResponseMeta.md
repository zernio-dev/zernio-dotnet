# Zernio.Model.ListInboxReviews200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountsQueried** | **int** |  | [optional] 
**AccountsFailed** | **int** |  | [optional] 
**FailedAccounts** | [**List&lt;ListInboxConversations200ResponseMetaFailedAccountsInner&gt;**](ListInboxConversations200ResponseMetaFailedAccountsInner.md) |  | [optional] 
**LastUpdated** | **DateTime** |  | [optional] 
**AccountsSkipped** | [**List&lt;ListInboxConversations200ResponseMetaAccountsSkippedInner&gt;**](ListInboxConversations200ResponseMetaAccountsSkippedInner.md) | Connected accounts that were not queried: their platform does not support this feature, or the account is not enabled for it | [optional] 
**TruncatedAccounts** | [**List&lt;ListInboxConversations200ResponseMetaAccountsSkippedInner&gt;**](ListInboxConversations200ResponseMetaAccountsSkippedInner.md) | Accounts whose listing hit the read budget with pages left: their reviews in data, and the Google Business Profile summary, are partial. Empty when every account was read in full. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

