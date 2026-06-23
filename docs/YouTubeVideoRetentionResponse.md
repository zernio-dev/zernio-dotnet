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
**RetentionCurve** | [**List&lt;YouTubeVideoRetentionResponseRetentionCurveInner&gt;**](YouTubeVideoRetentionResponseRetentionCurveInner.md) | Up to 100 points covering the video timeline, aggregated over the date range. Empty for videos with very few views. | [optional] 
**Note** | **string** | Present only when the curve is empty, explaining why | [optional] 
**ScopeStatus** | [**YouTubeDailyViewsResponseScopeStatus**](YouTubeDailyViewsResponseScopeStatus.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

