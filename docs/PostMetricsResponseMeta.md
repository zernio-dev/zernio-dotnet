# Zernio.Model.PostMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stale** | **bool** | True when the analytics backend was over capacity and part of this answer came from a stored copy instead of a live read. | 
**StaleSince** | **string** | With stale&#x3D;true: when the oldest stored copy used stopped being fresh. | 
**Entity** | **string** |  | 
**Granularity** | **string** |  | 
**FromDate** | **string** |  | 
**ToDate** | **string** |  | 
**MissingIds** | **List&lt;string&gt;** | Ids asked that match no published post the caller can read. | 
**Total** | **int?** |  | 
**SyncRequestedAccountIds** | **List&lt;string&gt;** | On a list of posts: the accounts this read queued for a fresh sync, because they were never synced or their stored numbers are over 90 minutes old. The answer holds the stored numbers; the synced ones arrive within minutes. | [optional] 
**AnalyticsOff** | [**List&lt;AnalyticsOffAccount&gt;**](AnalyticsOffAccount.md) | The X accounts read whose analytics sync does not run: their stored numbers are not refreshed, and their posts without any stay pending. On a list, on the first page. Absent when there are none, and on the groupBy and changedSince reads other than groupBy&#x3D;post. | [optional] 
**MetricsSample** | [**PostMetricsResponseMetaAllOfMetricsSample**](PostMetricsResponseMetaAllOfMetricsSample.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

