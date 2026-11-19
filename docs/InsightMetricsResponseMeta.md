# Zernio.Model.InsightMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Entity** | **string** |  | 
**AccountId** | **string** |  | 
**PlatformPostId** | **string** |  | 
**Platform** | **string** |  | 
**Granularity** | **string** |  | 
**GroupBy** | **string** | none, demographic, hour, keyword, or the Search Console dimensions grouped, such as query,country. | 
**Timeframe** | **string** | Instagram demographics: the period Instagram aggregated. | 
**FromDate** | **string** | Null for a lifetime or snapshot demographic breakdown. | 
**ToDate** | **string** |  | 
**UnavailableMetrics** | [**List&lt;InsightMetricsResponseMetaUnavailableMetricsInner&gt;**](InsightMetricsResponseMetaUnavailableMetricsInner.md) | Metrics asked that the platform could not answer for this account, with the reason. | 
**Units** | [**Dictionary&lt;string, InsightMetricsResponseMetaUnitsValue&gt;**](InsightMetricsResponseMetaUnitsValue.md) | Monetary metrics: the unit and currency the platform reports them in. Demographic metrics: count, share (0 to 1) or percent (0 to 100). | 
**DataDelay** | **string** | How late the platform reports these metrics, in words. Search Console: the rows cover final days only. | 
**ProvisionalSince** | **string** | First day the platform may still revise or have missing. Post insights only; null on account insights and when every day is final. | 
**Stale** | **bool** | True when the platform refused the refresh and the answer is the last stored copy. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

