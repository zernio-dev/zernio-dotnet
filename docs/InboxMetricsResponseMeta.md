# Zernio.Model.InboxMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stale** | **bool** | True when the analytics backend was over capacity and part of this answer came from a stored copy instead of a live read. | 
**StaleSince** | **string** | With stale&#x3D;true: when the oldest stored copy used stopped being fresh. | 
**Entity** | **string** |  | 
**Granularity** | **string** |  | 
**GroupBy** | **List&lt;string&gt;** |  | 
**FromDate** | **string** |  | 
**ToDate** | **string** |  | 
**Total** | **int?** | With groupBy&#x3D;conversation and include&#x3D;total: the conversations the list holds, up to 100,000. | 
**TotalIsCapped** | **bool** | true when the conversation list holds more than 100,000 conversations. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

