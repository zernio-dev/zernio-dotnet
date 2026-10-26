# Zernio.Model.GoogleAnalyticsReport
Google Analytics Data API report, passed through as Google returns it. Every value in `rows` is a string; read `metricHeaders[].type` to parse metrics.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio account ID of the Google Analytics connection. | [optional] 
**PropertyId** | **string** | Numeric GA4 property ID. | [optional] 
**DimensionHeaders** | [**List&lt;GoogleAnalyticsReportDimensionHeadersInner&gt;**](GoogleAnalyticsReportDimensionHeadersInner.md) |  | [optional] 
**MetricHeaders** | [**List&lt;GoogleAnalyticsReportMetricHeadersInner&gt;**](GoogleAnalyticsReportMetricHeadersInner.md) |  | [optional] 
**Rows** | [**List&lt;GoogleAnalyticsReportRowsInner&gt;**](GoogleAnalyticsReportRowsInner.md) |  | [optional] 
**RowCount** | **int** | Total rows matching the request, across all pages. | [optional] 
**Metadata** | **Dictionary&lt;string, Object&gt;** | Google report metadata (currency, time zone, sampling and thresholding flags). | [optional] 
**PropertyQuota** | **Dictionary&lt;string, Object&gt;** | Google quota left on this property after the request (tokens per day and per hour, concurrent requests). Cached responses carry the quota from when they were fetched. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

