# Zernio.Model.FacebookOrInstagramPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Facebook post id ({pageId}_{postId}) or Instagram media id | 
**Permalink** | **string** |  | 
**Text** | **string** | Facebook post message or Instagram caption | 
**ThumbnailUrl** | **string** | Facebook &#x60;full_picture&#x60; (or the first attachment image); Instagram &#x60;thumbnail_url&#x60; for videos, &#x60;media_url&#x60; for images. Expiring Meta CDN URL. | 
**MediaUrl** | **string** | Instagram &#x60;media_url&#x60; (the video file for videos). Always null on Facebook. Expiring Meta CDN URL. | 
**MediaType** | **string** | Instagram &#x60;media_type&#x60; (IMAGE, VIDEO, CAROUSEL_ALBUM) or the Facebook attachment type (photo, video_inline, link, ...) | 
**ProductType** | **string** | Instagram &#x60;media_product_type&#x60;: AD, FEED, REELS or STORY. Always null on Facebook. | 
**CreatedAt** | **string** | Creation time as Meta returns it (e.g. 2026-05-27T17:15:51+0000) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

