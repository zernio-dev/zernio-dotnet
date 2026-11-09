# Zernio.Model.YouTubeDailyViewsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** |  | [optional] 
**VideoId** | **string** | The YouTube video ID | [optional] 
**DurationSeconds** | **int?** | Video length in seconds (from YouTube contentDetails.duration) | [optional] 
**DateRange** | [**YouTubeDailyViewsResponseDateRange**](YouTubeDailyViewsResponseDateRange.md) |  | [optional] 
**ProvisionalSince** | **DateOnly** | Present only when the range reaches into YouTube&#39;s ~3-day processing window: the first date whose numbers are provisional and may still be revised by YouTube. | [optional] 
**TotalViews** | **int** | Sum of views across all days in the range | [optional] 
**Stale** | **bool** | Present and true when YouTube refused the refresh (the Analytics quota or its rate limit) and the response serves the days Zernio already stored, so some days may be missing; lastSyncedAt says how old they are. Retry later for a full refresh. | [optional] 
**DailyViews** | [**List&lt;YouTubeDailyViewsResponseDailyViewsInner&gt;**](YouTubeDailyViewsResponseDailyViewsInner.md) |  | [optional] 
**LastSyncedAt** | **DateTime?** | When the data was last synced from YouTube | [optional] 
**ScopeStatus** | [**YouTubeDailyViewsResponseScopeStatus**](YouTubeDailyViewsResponseScopeStatus.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

