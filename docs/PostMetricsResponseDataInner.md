# Zernio.Model.PostMetricsResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **string** | The day, with granularity&#x3D;day. | [optional] 
**PostId** | **string** |  | 
**ExternalPostId** | **string** |  | 
**AccountId** | **string** |  | 
**ProfileId** | **string** |  | 
**Platform** | **string** |  | 
**PlatformPostId** | **string** |  | 
**PlatformPostUrl** | **string** |  | 
**PublishedAt** | **string** |  | 
**LastSyncedAt** | **string** |  | 
**SyncStatus** | **string** |  | 
**SyncError** | [**PostMetricRowSyncError**](PostMetricRowSyncError.md) |  | 
**IsOwner** | **bool** |  | 
**IsAd** | **bool** |  | 
**Metrics** | **Dictionary&lt;string, decimal&gt;** | Each metric asked, as the platform reported it in this change; null when the post&#39;s platform does not report it. | 
**Breakdowns** | [**Dictionary&lt;string, PostMetricRowBreakdownsValue&gt;**](PostMetricRowBreakdownsValue.md) |  | [optional] 
**Post** | [**PostMetricContent**](PostMetricContent.md) |  | [optional] 
**Authenticity** | [**PostMetricAuthenticity**](PostMetricAuthenticity.md) |  | [optional] 
**Samples** | [**List&lt;PostMetricSample&gt;**](PostMetricSample.md) | With include&#x3D;samples: the readings of the publication, oldest first. | [optional] 
**Platforms** | **List&lt;string&gt;** |  | 
**AccountIds** | **List&lt;string&gt;** |  | 
**Publications** | **int** |  | 
**DayOfWeek** | **int** | UTC weekday the posts were published, 1 (Monday) to 7. | 
**Hour** | **int** | UTC hour the posts were published, 0 to 23. | 
**PostCount** | **int** | Posts of the format published in the range. | 
**PostAge** | **string** | Time since publishing: 0-6h, 6-12h, 12-24h, 1-2d, 2-7d, 7-30d or 30d+. | 
**Format** | **string** | gif counts as image, document as text. | 
**SyncedAt** | **string** | When the account&#39;s sync cycle that read these numbers started. Not an order: resume with the cursor only. | 
**Deleted** | **bool** | True when the post was removed from the platform. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

