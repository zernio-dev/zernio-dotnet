# Zernio.Model.AccountMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **string** | Start of the period: the day, the Monday of the week or the first of the month, never before fromDate. With granularity&#x3D;total, fromDate. | 
**AccountId** | **string** | With groupBy&#x3D;account. | 
**Platform** | **string** | With groupBy&#x3D;account or groupBy&#x3D;platform. | 
**ProfileId** | **string** | With groupBy&#x3D;account. | 
**Username** | **string** | With groupBy&#x3D;account. | 
**Metrics** | **Dictionary&lt;string, decimal?&gt;** | Each metric asked; null when no account in the row reports it or no follower snapshot exists in the period. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

