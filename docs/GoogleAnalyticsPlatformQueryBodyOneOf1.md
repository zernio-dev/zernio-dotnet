# Zernio.Model.GoogleAnalyticsPlatformQueryBodyOneOf1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ReportType** | **string** | A GA4 realtime report on the last 30 minutes, one page. | 
**AccountId** | **string** | The Zernio id of the connected Google Analytics property. | 
**Dimensions** | **List&lt;string&gt;** | GA4 dimension names, up to 9. | [optional] 
**Metrics** | **List&lt;string&gt;** | GA4 metric names, 1 to 10. | 
**DimensionFilter** | **Dictionary&lt;string, Object&gt;** | A GA4 FilterExpression on dimensions, sent to Google unchanged. | [optional] 
**MetricFilter** | **Dictionary&lt;string, Object&gt;** | A GA4 FilterExpression on metrics, sent to Google unchanged. | [optional] 
**OrderBys** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** | GA4 OrderBy objects, up to 10. | [optional] 
**Limit** | **int** | Rows, up to 10,000. | [optional] 
**MinuteRanges** | [**List&lt;GoogleAnalyticsPlatformQueryBodyOneOf1MinuteRangesInner&gt;**](GoogleAnalyticsPlatformQueryBodyOneOf1MinuteRangesInner.md) | Up to 2 GA4 minute ranges. Defaults to the last 30 minutes. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

