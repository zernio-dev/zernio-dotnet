# Zernio.Model.ExternalPostWebhookPost
Native (external) post data shared by all post.external.* payloads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native post ID (NOT a Zernio post ID). | 
**Platform** | **string** | Platform the post lives on (e.g. \&quot;googlebusiness\&quot;). | 
**AccountId** | **string** | Zernio social account ID the post belongs to. | 
**Url** | **string** | Direct URL to the post on the platform, when available. | 
**Content** | **string** | Post text. May be empty. | 
**MediaType** | **string** | One of image, video, gif, document, text, carousel. | 
**MediaItems** | [**List&lt;ExternalPostMediaItem&gt;**](ExternalPostMediaItem.md) |  | 
**ThumbnailUrl** | **string** |  | 
**PublishedAt** | **DateTime** |  | 
**MediaProductType** | **string** | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional] 
**IsAiGenerated** | **bool** | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional] 
**IsSharedToFeed** | **bool** | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional] 
**MediaAudioType** | **string** | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional] 
**Source** | **string** | Always \&quot;external\&quot; — distinguishes these from Zernio-originated post.* events. | 
**DeletedAt** | **DateTime?** | Detection time of deletion. Present on post.external.deleted; null/absent otherwise. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

