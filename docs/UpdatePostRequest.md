# Zernio.Model.UpdatePostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** | Stored on the post for reference/display only. This field is NOT used as the video title when publishing. To set a YouTube video title, use platformSpecificData.title on the youtube platform target (falls back to the first line of content when omitted). | [optional] 
**Content** | **string** |  | [optional] 
**MediaItems** | [**List&lt;MediaItem&gt;**](MediaItem.md) |  | [optional] 
**Platforms** | [**List&lt;UpdatePostRequestPlatformsInner&gt;**](UpdatePostRequestPlatformsInner.md) | Target platforms and accounts for this post. Each item must include platform and accountId. | [optional] 
**ScheduledFor** | **DateTime** |  | [optional] 
**PublishNow** | **bool** |  | [optional] [default to false]
**IsDraft** | **bool** | When omitted, the post keeps its current draft status. Send &#x60;false&#x60; to promote a draft to scheduled (combined with &#x60;scheduledFor&#x60;, &#x60;publishNow&#x60;, or a queue). | [optional] 
**Timezone** | **string** |  | [optional] 
**Visibility** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**Hashtags** | **List&lt;string&gt;** | Stored for reference only. Hashtags are NOT automatically appended to the caption when publishing. Include hashtags directly in the content field (platforms like Instagram only support hashtags as caption text). For YouTube keywords, use the tags field instead. | [optional] 
**Mentions** | **List&lt;string&gt;** |  | [optional] 
**CrosspostingEnabled** | **bool** |  | [optional] 
**Metadata** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**QueuedFromProfile** | **string** | Profile ID to schedule via queue. | [optional] 
**QueueId** | **string** | Specific queue ID to use when scheduling via queue. | [optional] 
**TiktokSettings** | [**TikTokPlatformData**](TikTokPlatformData.md) | Root-level TikTok settings applied to the TikTok platforms sent in the same request. Merged into each platform&#39;s platformSpecificData, with platform-specific settings taking precedence. Returns 400 if sent without a platforms array. | [optional] 
**FacebookSettings** | [**FacebookSettings**](FacebookSettings.md) | Root-level Facebook settings applied to the Facebook platforms sent in the same request. Merged into each platform&#39;s platformSpecificData.facebookSettings, with platform-specific settings taking precedence. Returns 400 if sent without a platforms array. | [optional] 
**Recycling** | [**RecyclingConfig**](RecyclingConfig.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

