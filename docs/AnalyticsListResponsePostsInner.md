# Zernio.Model.AnalyticsListResponsePostsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**LatePostId** | **string** | Original Zernio post ID if scheduled via Zernio | [optional] 
**Content** | **string** |  | [optional] 
**ScheduledFor** | **DateTime** |  | [optional] 
**PublishedAt** | **DateTime** |  | [optional] 
**Status** | **string** |  | [optional] 
**Analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] 
**Platforms** | [**List&lt;PlatformAnalytics&gt;**](PlatformAnalytics.md) |  | [optional] 
**Platform** | **string** |  | [optional] 
**PlatformPostUrl** | **string** |  | [optional] 
**IsExternal** | **bool** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**ThumbnailUrl** | **string** |  | [optional] 
**MediaType** | **string** |  | [optional] 
**MediaItems** | [**List&lt;AnalyticsListResponsePostsInnerMediaItemsInner&gt;**](AnalyticsListResponsePostsInnerMediaItemsInner.md) | All media items for this post. Carousel posts contain one entry per slide. | [optional] 
**MediaProductType** | **string** | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional] 
**IsAiGenerated** | **bool** | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional] 
**IsSharedToFeed** | **bool** | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional] 
**MediaAudioType** | **string** | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

