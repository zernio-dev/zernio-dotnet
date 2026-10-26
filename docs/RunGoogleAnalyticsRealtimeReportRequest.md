# Zernio.Model.RunGoogleAnalyticsRealtimeReportRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio account ID of the Google Analytics connection (platform &#x60;googleanalytics&#x60;). | 
**Dimensions** | **List&lt;string&gt;** | GA4 dimension API names, e.g. &#x60;date&#x60;, &#x60;sessionSource&#x60;, &#x60;pagePath&#x60;. List them with GET /v1/analytics/googleanalytics/metadata. | [optional] 
**Metrics** | **List&lt;string&gt;** | GA4 metric API names, e.g. &#x60;sessions&#x60;, &#x60;activeUsers&#x60;, &#x60;keyEvents&#x60;, &#x60;totalRevenue&#x60;. | 
**DimensionFilter** | **Dictionary&lt;string, Object&gt;** | A Google FilterExpression on dimensions, in Google&#39;s own shape. | [optional] 
**MetricFilter** | **Dictionary&lt;string, Object&gt;** | A Google FilterExpression on metrics, in Google&#39;s own shape. | [optional] 
**OrderBys** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** | Google OrderBy objects, e.g. &#x60;{ \&quot;metric\&quot;: { \&quot;metricName\&quot;: \&quot;sessions\&quot; }, \&quot;desc\&quot;: true }&#x60;. | [optional] 
**Limit** | **int** | Rows to return. Defaults to Google&#39;s default (10000). | [optional] 
**MinuteRanges** | [**List&lt;RunGoogleAnalyticsRealtimeReportRequestAllOfMinuteRangesInner&gt;**](RunGoogleAnalyticsRealtimeReportRequestAllOfMinuteRangesInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

