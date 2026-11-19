# Zernio.Model.InsightRetentionCurve

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromDate** | **string** | fromDate when given; otherwise the publish date, so the curve covers the video lifetime. | 
**ToDate** | **string** |  | 
**ProvisionalSince** | **string** |  | 
**DurationSeconds** | **decimal?** |  | 
**SegmentMetricsAvailable** | **bool** | False when YouTube has no startedWatching and stoppedWatching for the video; they read 0. | 
**Points** | [**List&lt;InsightRetentionPoint&gt;**](InsightRetentionPoint.md) | Up to 100 points, ascending; empty when YouTube has no curve, as on videos with very few views. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

