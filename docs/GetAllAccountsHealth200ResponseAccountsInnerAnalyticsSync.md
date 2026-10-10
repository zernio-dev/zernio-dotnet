# Zernio.Model.GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync
Absent on platforms without analytics sync. failing: several consecutive sync attempts failed. stalled: a sync was requested over 6 hours ago and never completed. never_synced: no sync has completed yet. Failing and stalled raise the account status to at least warning.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** |  | [optional] 
**LastSyncedAt** | **DateTime?** | Last successful sync. Null when never synced or the latest attempt failed. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

