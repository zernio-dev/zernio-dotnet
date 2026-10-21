# Zernio.Model.UpdatePostRequestPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AccountId** | **string** |  | 
**CustomContent** | **string** | Platform-specific text override. | [optional] 
**CustomMedia** | [**List&lt;MediaItem&gt;**](MediaItem.md) |  | [optional] 
**ScheduledFor** | **DateTime** | Optional per-platform scheduled time override. It is kept when a top-level scheduledFor is also sent, except a date sent back unchanged that matched the post scheduled time or is already past, which follows the new top-level scheduledFor. | [optional] 
**PlatformSpecificData** | **Dictionary&lt;string, Object&gt;** | A &lt;platform&gt;Settings namespace (e.g. facebookSettings, tiktokSettings) omitted from the request is preserved from the stored post. Sending the key replaces the whole namespace; it is not deep-merged. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

