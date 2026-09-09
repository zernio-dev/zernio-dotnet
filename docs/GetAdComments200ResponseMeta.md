# Zernio.Model.GetAdComments200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** | Platform of the comments. | 
**Placement** | **string** | The placement these comments are for, useful when you didn&#39;t pass ?placement&#x3D; and want to know which one you got. | [optional] 
**AdId** | **string** | Internal Zernio ad ID. | 
**PlatformAdId** | **string** | Platform ad ID. | [optional] 
**EffectiveStoryId** | **string** | Underlying post ID the comments belong to. effective_object_story_id for the Facebook side, effective_instagram_media_id for the Instagram side. | [optional] 
**TiktokItemId** | **string** | TikTok-only video item ID. Null when the ad and comments do not expose it. | [optional] 
**Since** | **DateOnly** | TikTok-only resolved start date. | [optional] 
**Until** | **DateOnly** | TikTok-only resolved end date. | [optional] 
**FacebookAccountId** | **string** | Facebook-only. The connected Facebook Page SocialAccount these comments were read through. Pass it as &#x60;accountId&#x60; (with &#x60;effectiveStoryId&#x60; as the postId) to /v1/inbox/comments to reply/hide/delete. Null when no connected Page was used (then moderation isn&#39;t possible). | [optional] 
**InstagramUserId** | **string** | Instagram-only. The Instagram-scoped business ID that owns the boosted media (creative.instagram_user_id). | [optional] 
**InstagramPermalink** | **string** | Instagram-only. Public permalink of the boosted IG post (creative.instagram_permalink_url). | [optional] 
**InstagramAccountId** | **string** | Instagram-only. The connected Instagram SocialAccount these comments were read through. Pass it as &#x60;accountId&#x60; (with &#x60;effectiveStoryId&#x60; as the postId) to /v1/inbox/comments to reply/hide/delete. | [optional] 
**AccountId** | **string** | Account ID (ads SocialAccount). | 
**LastUpdated** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

