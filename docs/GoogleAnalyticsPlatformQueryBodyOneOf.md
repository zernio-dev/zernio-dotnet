# Zernio.Model.GoogleAnalyticsPlatformQueryBodyOneOf

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ReportType** | **string** | A GA4 report over date ranges, paged with a cursor. | 
**AccountId** | **string** | The Zernio id of the connected Google Analytics property. | 
**Dimensions** | **List&lt;string&gt;** | GA4 dimension names, up to 9. | [optional] 
**Metrics** | **List&lt;string&gt;** | GA4 metric names, 1 to 10. | 
**DimensionFilter** | **Dictionary&lt;string, Object&gt;** | A GA4 FilterExpression on dimensions, sent to Google unchanged. | [optional] 
**MetricFilter** | **Dictionary&lt;string, Object&gt;** | A GA4 FilterExpression on metrics, sent to Google unchanged. | [optional] 
**OrderBys** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** | GA4 OrderBy objects, up to 10. | [optional] 
**Limit** | **int** | Rows per page, up to 10,000. Defaults to 10,000. | [optional] [default to 10000]
**DateRanges** | [**List&lt;GoogleAnalyticsPlatformQueryBodyOneOfDateRangesInner&gt;**](GoogleAnalyticsPlatformQueryBodyOneOfDateRangesInner.md) | Up to 4 GA4 date ranges. Defaults to the 28 days ending yesterday. | [optional] 
**KeepEmptyRows** | **bool** | Keep rows whose metrics are all 0. | [optional] 
**CurrencyCode** | **string** | ISO 4217 code for money metrics. | [optional] 
**Cursor** | **string** | The pagination.nextCursor of the previous page, unchanged. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

