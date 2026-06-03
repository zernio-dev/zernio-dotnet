# Zernio.Model.UpdatePostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | [optional] 
**Content** | **string** |  | [optional] 
**MediaItems** | [**List&lt;MediaItem&gt;**](MediaItem.md) |  | [optional] 
**Platforms** | [**List&lt;UpdatePostRequestPlatformsInner&gt;**](UpdatePostRequestPlatformsInner.md) | Target platforms and accounts for this post. Each item must include platform and accountId. | [optional] 
**ScheduledFor** | **DateTime** |  | [optional] 
**PublishNow** | **bool** |  | [optional] [default to false]
**IsDraft** | **bool** |  | [optional] 
**Timezone** | **string** |  | [optional] 
**Visibility** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**Hashtags** | **List&lt;string&gt;** |  | [optional] 
**Mentions** | **List&lt;string&gt;** |  | [optional] 
**CrosspostingEnabled** | **bool** |  | [optional] 
**Metadata** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**QueuedFromProfile** | **string** | Profile ID to schedule via queue. | [optional] 
**QueueId** | **string** | Specific queue ID to use when scheduling via queue. | [optional] 
**TiktokSettings** | [**TikTokPlatformData**](TikTokPlatformData.md) | Root-level TikTok settings applied to all TikTok platforms. Merged into each platform&#39;s platformSpecificData, with platform-specific settings taking precedence. | [optional] 
**FacebookSettings** | [**FacebookPlatformData**](FacebookPlatformData.md) | Root-level Facebook settings applied to all Facebook platforms. Merged into each platform&#39;s platformSpecificData, with platform-specific settings taking precedence. | [optional] 
**Recycling** | [**RecyclingConfig**](RecyclingConfig.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

