# Zernio.Model.PostMetricContent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Content** | **string** |  | 
**ContentNotRetained** | **bool** |  | [optional] 
**ThumbnailUrl** | **string** |  | 
**MediaType** | **string** |  | 
**MediaItems** | [**List&lt;PostMetricMediaItem&gt;**](PostMetricMediaItem.md) |  | 
**VideoDurationSeconds** | **decimal?** |  | 
**MediaProductType** | **string** |  | [optional] 
**IsAiGenerated** | **bool** |  | [optional] 
**IsSharedToFeed** | **bool** |  | [optional] 
**MediaAudioType** | **string** |  | [optional] 
**UpcomingStartAt** | **DateTime** | YouTube only. Start time of an upcoming Premiere or scheduled live stream. Absent once it airs. While it is present, publishedAt is the upload time; after it airs, publishedAt is the time it actually started. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

