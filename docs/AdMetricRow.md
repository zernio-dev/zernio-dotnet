# Zernio.Model.AdMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdId** | **string** |  | 
**Name** | **string** |  | 
**Platform** | **string** |  | 
**Status** | **string** |  | 
**Currency** | **string** |  | 
**Summary** | [**AdMetricRowSummary**](AdMetricRowSummary.md) |  | 
**Daily** | [**List&lt;AdMetricRowDailyInner&gt;**](AdMetricRowDailyInner.md) | With granularity&#x3D;day: one point per day. | [optional] 
**Breakdowns** | **Dictionary&lt;string, Object&gt;** | With breakdowns: read live from the platform. | [optional] 
**UnsupportedBreakdowns** | **List&lt;string&gt;** |  | [optional] 
**BreakdownHints** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**BreakdownsRange** | **Object** |  | [optional] 
**BreakdownErrors** | **List&lt;Object&gt;** |  | [optional] 
**BreakdownDroppedMetrics** | **Dictionary&lt;string, List&lt;string&gt;&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

