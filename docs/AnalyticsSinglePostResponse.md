# Zernio.Model.AnalyticsSinglePostResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PostId** | **string** |  | [optional] 
**LatePostId** | **string** | Original Zernio post ID if scheduled via Zernio | [optional] 
**Status** | **string** | Overall post status. \&quot;partial\&quot; when some platforms published and others failed.  While any platform is still pending or processing, the post&#39;s own status is returned instead (usually scheduled or publishing), even if another platform already published.  A post with no published or failed platform (for example every platform cancelled) returns its own status with syncStatus unavailable and no platformAnalytics. | [optional] 
**Content** | **string** |  | [optional] 
**ContentNotRetained** | **bool** | True when this team does not retain content, so the content fields of this row are null. Identifiers and metadata stay. | [optional] 
**ScheduledFor** | **DateTime** |  | [optional] 
**PublishedAt** | **DateTime?** |  | [optional] 
**Analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] 
**PlatformAnalytics** | [**List&lt;PlatformAnalytics&gt;**](PlatformAnalytics.md) |  | [optional] 
**Platform** | **string** |  | [optional] 
**PlatformPostUrl** | **string** |  | [optional] 
**IsExternal** | **bool** |  | [optional] 
**SyncStatus** | **string** | Overall sync state across all platforms | [optional] 
**Message** | **string** | Human-readable status message for pending, partial, or failed states | [optional] 
**AnalyticsOff** | [**List&lt;AnalyticsOffAccount&gt;**](AnalyticsOffAccount.md) | The X accounts of this post whose analytics sync does not run: synced numbers stay as of the last read, and a pending X entry stays pending. Absent when there are none. | [optional] 
**ThumbnailUrl** | **string** | Cover image URL. A Facebook, Instagram or TikTok cover whose signed CDN link is still valid is served as that link, which expires (Meta &#x60;oe&#x3D;&#x60;, TikTok &#x60;x-expires&#x3D;&#x60;): download the image rather than storing the link.  Once the link expires, Zernio re-reads the cover from the platform and serves it from Zernio storage, a URL that does not expire.  Null while that re-read is pending (read again shortly) or when the platform no longer returns the post, never an expired link. | [optional] 
**MediaType** | **string** |  | [optional] 
**MediaItems** | [**List&lt;AnalyticsSinglePostResponseMediaItemsInner&gt;**](AnalyticsSinglePostResponseMediaItemsInner.md) | All media items for this post. Carousel posts have one entry per slide.  - Facebook and Instagram images and video covers whose Meta CDN links expired are re-read and served from Zernio storage (non-expiring). - Facebook and Instagram video file URLs, and LinkedIn media URLs, stay the platform&#39;s signed links and are refreshed on read once they lapse. - A &#x60;url&#x60; or &#x60;thumbnail&#x60; whose platform link expired and could not be re-read yet is null, never the expired link.  | [optional] 
**MediaProductType** | **string** | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional] 
**IsAiGenerated** | **bool** | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional] 
**IsSharedToFeed** | **bool** | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional] 
**MediaAudioType** | **string** | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional] 
**UpcomingStartAt** | **DateTime** | YouTube only. Start time of an upcoming Premiere or scheduled live stream. Absent once it airs. While it is present, publishedAt is the upload time; after it airs, publishedAt is the time it actually started. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

