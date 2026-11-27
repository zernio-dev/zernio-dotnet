# Zernio.Model.UpdatePostRequestPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AccountId** | **string** |  | 
**CustomContent** | **string** | Platform-specific text override. | [optional] 
**CustomMedia** | [**List&lt;MediaItem&gt;**](MediaItem.md) | On update, an omitted customMedia keeps the stored per-platform media; send [] to clear it. | [optional] 
**ScheduledFor** | **DateTime** | Optional per-platform scheduled time override.  With a top-level scheduledFor in the same request, the override is kept. Exception: a date sent back unchanged (same instant, or same wall-clock time in the previous timezone) that matched the post time or is already past follows the new top-level scheduledFor.  When omitted, the entry takes the top-level scheduledFor. Without one, it keeps its current time if still in the future, otherwise the post&#39;s scheduledFor if in the future, otherwise the earliest scheduledFor sent in this request.  A past time is accepted and not published in the request. An entry due within the last 7 days is published at the next scheduler run; one more than 7 days in the past is not published and is marked failed. | [optional] 
**PlatformSpecificData** | **Dictionary&lt;string, Object&gt;** | A &lt;platform&gt;Settings namespace (e.g. facebookSettings, tiktokSettings) omitted from the request is preserved from the stored post. Sending the key replaces the whole namespace; it is not deep-merged. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

