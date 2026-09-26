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
**IsAd** | **bool** | True when this post&#39;s metrics include paid delivery, so organic reporting should exclude it. Set for LinkedIn dark posts and for TikTok posts that one of your TikTok ads promotes (Spark / boosted). TikTok exposes no ad flag of its own, so a video created by an uploaded-asset (non-Spark) TikTok ad is posted to the profile with a fresh organic id and cannot be detected: those still report as false. | [optional] 
**ProfileId** | **string** |  | [optional] 
**ThumbnailUrl** | **string** | Cover image URL. Facebook and Instagram covers whose Meta CDN link expired are re-read from Meta and served from Zernio storage, so that URL does not expire and can be cached. | [optional] 
**MediaType** | **string** |  | [optional] 
**MediaItems** | [**List&lt;AnalyticsListResponsePostsInnerMediaItemsInner&gt;**](AnalyticsListResponsePostsInnerMediaItemsInner.md) | All media items for this post. Carousel posts contain one entry per slide. Facebook and Instagram images and video covers whose Meta CDN links expired are re-read and served from Zernio storage (non-expiring). Facebook and Instagram video file URLs, and LinkedIn media URLs, stay the platform&#39;s signed links and are refreshed on read once they lapse. | [optional] 
**MediaProductType** | **string** | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional] 
**IsAiGenerated** | **bool** | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional] 
**IsSharedToFeed** | **bool** | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional] 
**MediaAudioType** | **string** | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

