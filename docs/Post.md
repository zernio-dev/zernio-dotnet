# Zernio.Model.Post

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**UserId** | [**PostUserId**](PostUserId.md) |  | [optional] 
**Title** | **string** | Stored on the post for reference/display only. This field is NOT used as the video title when publishing. To set a YouTube video title, use platformSpecificData.title on the youtube platform target (falls back to the first line of content when omitted). | [optional] 
**Content** | **string** |  | [optional] 
**MediaItems** | [**List&lt;MediaItem&gt;**](MediaItem.md) |  | [optional] 
**Platforms** | [**List&lt;PlatformTarget&gt;**](PlatformTarget.md) |  | [optional] 
**ScheduledFor** | **DateTime** |  | [optional] 
**Timezone** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** | YouTube constraints: each tag max 100 chars, combined max 500 chars, duplicates removed. | [optional] 
**Hashtags** | **List&lt;string&gt;** | Stored for reference only. Hashtags are NOT automatically appended to the caption when publishing. Include hashtags directly in the content field (platforms like Instagram only support hashtags as caption text). For YouTube keywords, use the tags field instead. | [optional] 
**Mentions** | **List&lt;string&gt;** | Stored for reference only. This field does NOT automatically create @mentions when publishing. For LinkedIn @mentions, use the /v1/accounts/{accountId}/linkedin-mentions endpoint to resolve profile URLs to URNs, then embed the returned mentionFormat directly in the post content field. | [optional] 
**Visibility** | **string** |  | [optional] 
**Metadata** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**Recycling** | [**RecyclingState**](RecyclingState.md) |  | [optional] 
**RecycledFromPostId** | **string** | ID of the original post if this post was created via recycling | [optional] 
**QueuedFromProfile** | **string** | Profile ID if the post was scheduled via the queue | [optional] 
**QueueId** | **string** | Queue ID if the post was scheduled via a specific queue | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

