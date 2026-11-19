# Zernio.Model.InsightMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **string** | The day with granularity&#x3D;day; fromDate with granularity&#x3D;total; null for a lifetime total. With groupBy&#x3D;demographic, the day the breakdown describes (meta.toDate). With groupBy&#x3D;keyword, the first day of the months reported (meta.fromDate). | 
**Breakdown** | **string** | With groupBy: the segment kind, such as age, country, hour or keyword; on Search Console, the dimensions grouped, such as query,country. | 
**Dimension** | **string** | With groupBy: the segment value, such as 25-34, US, the hour 0 to 23 as Instagram reports it, or the search keyword. Search Console: the value when one dimension is grouped, null otherwise (see dimensions). | 
**DimensionId** | **string** | With groupBy&#x3D;demographic on LinkedIn: the platform id of the segment. | 
**Dimensions** | **Dictionary&lt;string, string&gt;** | Search Console with groupBy: the value of each dimension, such as { query, country }. country is an ISO 3166-1 alpha-3 code in lowercase; device is DESKTOP, MOBILE or TABLET. | [optional] 
**Metrics** | **Dictionary&lt;string, decimal?&gt;** | Each metric asked; null when the platform did not report it for the period. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

