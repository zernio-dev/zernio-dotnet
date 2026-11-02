# Zernio.Model.YouTubeVideoRetentionResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** |  | [optional] 
**AccountId** | **string** | The Zernio account ID for the YouTube account | [optional] 
**VideoId** | **string** | The YouTube video ID | [optional] 
**Title** | **string** | Video title | [optional] 
**PublishedAt** | **DateTime?** | When the video was published on YouTube | [optional] 
**DurationSeconds** | **int?** | Video length in seconds (from YouTube contentDetails.duration) | [optional] 
**DateRange** | [**YouTubeDailyViewsResponseDateRange**](YouTubeDailyViewsResponseDateRange.md) |  | [optional] 
**ProvisionalSince** | **DateOnly** | Present only when the range reaches into YouTube&#39;s ~3-day processing window: the first date whose numbers are provisional and may still be revised by YouTube. | [optional] 
**SegmentMetricsAvailable** | **bool** | Whether YouTube returned startedWatching and stoppedWatching for this curve. When false, both are 0 placeholders in every point, not measured values. | [optional] 
**RetentionCurve** | [**List&lt;YouTubeVideoRetentionResponseRetentionCurveInner&gt;**](YouTubeVideoRetentionResponseRetentionCurveInner.md) | Up to 100 points covering the video timeline, aggregated over the date range. Contains only the buckets YouTube reports for that range and is never zero-filled, so it can end before 1.0, skip positions, or be empty. | [optional] 
**Note** | **string** | Present only when the curve is empty, explaining why | [optional] 
**ScopeStatus** | [**YouTubeDailyViewsResponseScopeStatus**](YouTubeDailyViewsResponseScopeStatus.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

