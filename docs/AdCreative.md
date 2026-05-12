# Zernio.Model.AdCreative
Platform-specific creative data. Fields vary by platform.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ThumbnailUrl** | **string** | Primary thumbnail/image URL | [optional] 
**ImageUrl** | **string** | Alternative image URL | [optional] 
**VideoId** | **string** | Meta video ID for VIDEO-type ads. Null for non-video ads. Callers that need an embeddable MP4 can call GET /{videoId}?fields&#x3D;source with the page access token. | [optional] 
**VideoUrl** | **string** | Public Facebook watch URL for VIDEO-type ads (https://www.facebook.com/watch/?v&#x3D;{videoId}). Null for non-video ads. | [optional] 
**ObjectType** | **string** | Meta creative object_type (e.g. SHARE, VIDEO, PRIVACY_CHECK_FAIL, POST_DELETED). Use this to render state-aware previews — when Meta moderation strips image/video fields, only thumbnailUrl at 64x64 is available. | [optional] 
**ObjectStoryId** | **string** | Meta creative &#x60;object_story_id&#x60; (the SHARE reference). Frequently absent — Meta omits it for SHARE creatives. Use effectiveObjectStoryId instead. | [optional] 
**EffectiveObjectStoryId** | **string** | Meta &#x60;effective_object_story_id&#x60; — &#x60;{pageId}_{postId}&#x60; of the Facebook post the ad&#39;s engagement (comments) lives on. Pass to GET /v1/ads?effectiveObjectStoryId&#x3D; to map a Business-Manager-visible post back to this ad; GET /v1/ads/{adId}/comments resolves comments against it. | [optional] 
**EffectiveInstagramMediaId** | **string** | Meta &#x60;effective_instagram_media_id&#x60; — the Instagram media ID of the boosted post the ad&#39;s engagement lives on. Pass to GET /v1/ads?effectiveInstagramMediaId&#x3D; to map a Business-Manager-visible IG post back to this ad. | [optional] 
**InstagramUserId** | **string** | Meta &#x60;instagram_user_id&#x60; — the Instagram-scoped business ID that owns the boosted media. | [optional] 
**InstagramPermalinkUrl** | **string** | Meta &#x60;instagram_permalink_url&#x60; — public Instagram post URL of the boosted media. | [optional] 
**MediaUrls** | **List&lt;string&gt;** | All media URLs for this ad (carousel images, multiple assets). Populated for Meta (carousel child_attachments), Google Ads (responsive display marketing_images), and LinkedIn (multi-image posts). | [optional] 
**Body** | **string** | Ad copy/text | [optional] 
**GoogleHeadline** | **string** | Google Ads headline | [optional] 
**GoogleDescription** | **string** | Google Ads description | [optional] 
**LinkUrl** | **string** | Destination URL | [optional] 
**PinterestImageUrl** | **string** |  | [optional] 
**PinterestTitle** | **string** |  | [optional] 
**PinterestDescription** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

