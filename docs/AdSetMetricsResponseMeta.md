# Zernio.Model.AdSetMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stale** | **bool** | True when the analytics backend was over capacity and part of this answer came from a stored copy instead of a live read. | 
**StaleSince** | **string** | With stale&#x3D;true: when the oldest stored copy used stopped being fresh. | 
**FromDate** | **string** |  | 
**ToDate** | **string** |  | 
**MissingIds** | **List&lt;string&gt;** | With adSetId, asked ids that are not ad sets the caller can see. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

