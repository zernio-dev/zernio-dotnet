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
**MediaItems** | [**List&lt;ExternalPostWebhookPostMediaItemsInner&gt;**](ExternalPostWebhookPostMediaItemsInner.md) |  | 
**ThumbnailUrl** | **string** |  | 
**PublishedAt** | **DateTime** |  | 
**Source** | **string** | Always \&quot;external\&quot; — distinguishes these from Zernio-originated post.* events. | 
**DeletedAt** | **DateTime** | Detection time of deletion. Present on post.external.deleted; null/absent otherwise. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

