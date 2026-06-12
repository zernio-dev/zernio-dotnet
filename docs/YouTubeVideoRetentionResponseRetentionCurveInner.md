# Zernio.Model.YouTubeVideoRetentionResponseRetentionCurveInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ElapsedVideoTimeRatio** | **decimal** | Position in the video as a ratio (0.01-1.0, exclusive end of each interval) | [optional] 
**AudienceWatchRatio** | **decimal** | Absolute share of viewers watching at this point. Can exceed 1 (rewinds/looping, common on Shorts). | [optional] 
**RelativeRetentionPerformance** | **decimal** | Retention vs videos of similar length (0 &#x3D; worst, 0.5 &#x3D; median, 1 &#x3D; best) | [optional] 
**StartedWatching** | **int** | Viewers who started watching in this segment | [optional] 
**StoppedWatching** | **int** | Viewers who stopped watching in this segment | [optional] 
**TotalSegmentImpressions** | **int** | Total views of this segment, including rewatches | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

