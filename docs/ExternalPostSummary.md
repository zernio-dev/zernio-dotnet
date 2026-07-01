# Zernio.Model.ExternalPostSummary
A post synced from a platform (published directly on the platform, not through Zernio). Returned by GET /v1/posts?source=external and POST /v1/posts/sync-external. Analytics are exposed separately via GET /v1/analytics?source=external. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** | Platform the post belongs to (e.g. instagram, youtube, tiktok) | [optional] 
**PlatformPostId** | **string** | The platform&#39;s own post/media/video id | [optional] 
**PlatformPostUrl** | **string** | Canonical URL (permalink) of the post on the platform | [optional] 
**Content** | **string** | Post caption / text | [optional] 
**PublishedAt** | **DateTime** | When the post was published on the platform | [optional] 
**MediaType** | **string** | Media type (e.g. image, video, carousel) | [optional] 
**MediaUrl** | **string** | Primary media URL | [optional] 
**ThumbnailUrl** | **string** | Thumbnail URL | [optional] 
**MediaItems** | **List&lt;Object&gt;** | Per-item media (for carousels / multi-media posts) | [optional] 
**Analytics** | [**ExternalPostSummaryAnalytics**](ExternalPostSummaryAnalytics.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

