# Zernio.Model.GetAdComments200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** | Which side these comments are on (same as &#x60;placement&#x60;). | 
**Placement** | **string** | The placement these comments are for — useful when you didn&#39;t pass ?placement&#x3D; and want to know which one you got. | 
**AdId** | **string** | Internal Zernio ad ID. | 
**PlatformAdId** | **string** | Meta ad ID. | 
**EffectiveStoryId** | **string** | Underlying post ID the comments belong to. effective_object_story_id for the Facebook side, effective_instagram_media_id for the Instagram side. | 
**FacebookAccountId** | **string** | Facebook-only. The connected Facebook Page SocialAccount these comments were read through — pass it as &#x60;accountId&#x60; (with &#x60;effectiveStoryId&#x60; as the postId) to /v1/inbox/comments to reply/hide/delete. Null when no connected Page was used (then moderation isn&#39;t possible). | [optional] 
**InstagramUserId** | **string** | Instagram-only. The Instagram-scoped business ID that owns the boosted media (creative.instagram_user_id). | [optional] 
**InstagramPermalink** | **string** | Instagram-only. Public permalink of the boosted IG post (creative.instagram_permalink_url). | [optional] 
**InstagramAccountId** | **string** | Instagram-only. The connected Instagram SocialAccount these comments were read through — pass it as &#x60;accountId&#x60; (with &#x60;effectiveStoryId&#x60; as the postId) to /v1/inbox/comments to reply/hide/delete. | [optional] 
**AccountId** | **string** | Social account ID (ads SocialAccount). | 
**LastUpdated** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

