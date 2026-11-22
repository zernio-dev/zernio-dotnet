# Zernio.Model.GetAllAccountsHealth200ResponseAccountsInnerPublishingRestriction
Set when the last 3 finished publishes failed with the same account-level error (suspended, restricted, a verification check, an expired login). The next successful publish or a reconnect clears it. While set, status is at least `warning`. Null when the account publishes normally.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Reason** | **string** |  | [optional] 
**Message** | **string** | The stored error message of the last failed publish. | [optional] 
**Since** | **DateTime** |  | [optional] 
**LastFailedAt** | **DateTime** |  | [optional] 
**BlocksPublishNow** | **bool** | True while POST /v1/posts refuses publish-now posts to this account with 422 &#x60;account_restricted&#x60; (24 hours after the last failure). Scheduled posts are always accepted. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

