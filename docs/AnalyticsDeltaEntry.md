# Zernio.Model.AnalyticsDeltaEntry
One changed analytics snapshot. Metrics are the absolute values recorded at `syncedAt`, not the amount they moved by since the previous snapshot, so a later entry for the same `postId` always supersedes an earlier one. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PostId** | **string** | External post ID. The same identifier as &#x60;posts[]._id&#x60; in GET /v1/analytics. | 
**AccountId** | **string** | Social account this post was published through | 
**ProfileId** | **string** | Profile the account belongs to | 
**Platform** | **string** |  | 
**PlatformPostId** | **string** | Platform-side post ID (for example the YouTube video ID) | 
**PublishedAt** | **DateTime** | When the post was published, ISO-8601 UTC | 
**SyncedAt** | **DateTime** | When the sync cycle that produced this snapshot STARTED, ISO-8601 UTC. This is NOT the order entries arrive in and it is not a resume point: a slow cycle writes its rows after a faster cycle that started later, so &#x60;syncedAt&#x60; can go backwards between consecutive entries. Use &#x60;nextCursor&#x60; to resume.  | 
**IsDeleted** | **bool** | True when the post was detected as deleted on the platform at this sync | 
**Metrics** | [**AnalyticsDeltaEntryMetrics**](AnalyticsDeltaEntryMetrics.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

