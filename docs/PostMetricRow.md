# Zernio.Model.PostMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **string** | The day, with granularity&#x3D;day. | [optional] 
**PostId** | **string** | The Zernio post, null for a post published outside Zernio. | 
**ExternalPostId** | **string** | The synced post, null while a published post waits for its first sync. | 
**AccountId** | **string** |  | 
**ProfileId** | **string** |  | 
**Platform** | **string** |  | 
**PlatformPostId** | **string** |  | 
**PlatformPostUrl** | **string** |  | 
**PublishedAt** | **string** |  | 
**LastSyncedAt** | **string** |  | 
**SyncStatus** | **string** |  | 
**SyncError** | [**PostMetricRowSyncError**](PostMetricRowSyncError.md) |  | 
**IsOwner** | **bool?** |  | 
**IsAd** | **bool?** |  | 
**Metrics** | **Dictionary&lt;string, decimal?&gt;** | Each metric asked; null when the platform does not report it or no snapshot exists yet. | 
**Breakdowns** | [**Dictionary&lt;string, PostMetricRowBreakdownsValue&gt;**](PostMetricRowBreakdownsValue.md) |  | [optional] 
**Post** | [**PostMetricContent**](PostMetricContent.md) |  | [optional] 
**Authenticity** | [**PostMetricAuthenticity**](PostMetricAuthenticity.md) |  | [optional] 
**Samples** | [**List&lt;PostMetricSample&gt;**](PostMetricSample.md) | With include&#x3D;samples: the readings of the publication, oldest first. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

