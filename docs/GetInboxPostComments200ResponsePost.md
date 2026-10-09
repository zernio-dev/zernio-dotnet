# Zernio.Model.GetInboxPostComments200ResponsePost
(Reddit, Facebook and Instagram) Metadata for the target post, returned alongside the comments so integrators can render a preview of the post being commented on without an additional request.  Facebook and Instagram return the Meta shape: the post thumbnail, text and permalink, for any post the account can read, including the hidden dark posts Meta publishes for each variant of an ad (dynamic creative, placement asset customization, Advantage+). Facebook posts need the Facebook Page connection and Instagram media the Instagram connection. `thumbnailUrl` and `mediaUrl` are Meta CDN URLs that expire: store a copy if you render them later. On Instagram, `productType` tells an ad (`AD`) from organic media (`FEED`, `REELS`, `STORY`).  Absent on other platforms, when the post cannot be read with the connection's token, and on Reddit when the upstream response is missing the post listing (deleted post, malformed response). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Facebook post id ({pageId}_{postId}) or Instagram media id | 
**Fullname** | **string** | Fullname with type prefix (e.g. \&quot;t3_1tjtj26\&quot;) | [optional] 
**Title** | **string** |  | [optional] 
**Selftext** | **string** | Body text for self-posts (empty for link posts) | [optional] 
**Author** | **string** | Reddit username, without the u/ prefix | [optional] 
**Subreddit** | **string** | Subreddit name, without the r/ prefix | [optional] 
**Permalink** | **string** |  | 
**Url** | **string** | For link posts, the external URL; for self-posts, the Reddit permalink | [optional] 
**Score** | **int** | Net upvotes (upvotes minus downvotes) | [optional] 
**NumComments** | **int** |  | [optional] 
**CreatedUtc** | **int** | Unix timestamp in seconds | [optional] 
**Over18** | **bool** |  | [optional] 
**Stickied** | **bool** |  | [optional] 
**FlairText** | **string** | Link flair text if any | [optional] 
**IsGallery** | **bool** | True if the post is a Reddit gallery (multiple images) | [optional] 
**Text** | **string** | Facebook post message or Instagram caption | 
**ThumbnailUrl** | **string** | Facebook &#x60;full_picture&#x60; (or the first attachment image); Instagram &#x60;thumbnail_url&#x60; for videos, &#x60;media_url&#x60; for images. Expiring Meta CDN URL. | 
**MediaUrl** | **string** | Instagram &#x60;media_url&#x60; (the video file for videos). Always null on Facebook. Expiring Meta CDN URL. | 
**MediaType** | **string** | Instagram &#x60;media_type&#x60; (IMAGE, VIDEO, CAROUSEL_ALBUM) or the Facebook attachment type (photo, video_inline, link, ...) | 
**ProductType** | **string** | Instagram &#x60;media_product_type&#x60;: AD, FEED, REELS or STORY. Always null on Facebook. | 
**CreatedAt** | **string** | Creation time as Meta returns it (e.g. 2026-05-27T17:15:51+0000) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

