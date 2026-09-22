# Zernio.Model.CtwaAdRequestBodyCreativesInner
Supply headline, body, and image/video, or exactly one existing post reference. References cannot be combined with fresh creative fields.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformPostId** | **string** | Messaging and CTWA only. Platform post or reel ID, the same input boostPost takes as platformPostId. Facebook IDs become object_story_id; Instagram IDs become source_instagram_media_id using the connected Instagram identity. Mutually exclusive with objectStoryId and fresh creative fields. | [optional] 
**ExistingPostId** | **string** | Alias of platformPostId, kept for existing callers. Sending both with different values is a 400. | [optional] 
**ObjectStoryId** | **string** | Messaging and CTWA only. Raw Facebook pageId_postId reference, used as object_story_id even with an Instagram account. Mutually exclusive with platformPostId and fresh creative fields. | [optional] 
**CreativeFeatures** | **Dictionary&lt;string, CtwaAdRequestBodyCreativesInner.InnerEnum&gt;** | Replaces the top-level creativeFeatures map for this item. Omit to inherit; an empty object clears inherited enrollment choices. | [optional] 
**Headline** | **string** |  | [optional] 
**Body** | **string** | Primary text shown above the image / video. | [optional] 
**ImageUrl** | **string** | Image asset. Mutually exclusive with this entry&#39;s &#x60;video&#x60;. Required if neither &#x60;video&#x60; nor an existing post reference is supplied.  | [optional] 
**Video** | [**CtwaAdRequestBodyCreativesInnerVideo**](CtwaAdRequestBodyCreativesInnerVideo.md) |  | [optional] 
**WelcomeMessage** | [**CtwaAdRequestBodyCreativesInnerWelcomeMessage**](CtwaAdRequestBodyCreativesInnerWelcomeMessage.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

