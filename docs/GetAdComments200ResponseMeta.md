# Zernio.Model.GetAdComments200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**AdId** | **string** | Internal Zernio ad ID. | 
**PlatformAdId** | **string** | Meta ad ID. | 
**EffectiveStoryId** | **string** | Underlying post ID the comments belong to. effective_object_story_id for Facebook, effective_instagram_media_id for Instagram. | 
**InstagramUserId** | **string** | Instagram-only. The Instagram-scoped business ID that owns the boosted media (creative.instagram_user_id). | [optional] 
**InstagramPermalink** | **string** | Instagram-only. Public permalink of the boosted IG post (creative.instagram_permalink_url). | [optional] 
**InstagramAccountId** | **string** | Instagram-only. The connected Instagram SocialAccount these comments were read through — use it for reply/hide actions via /v1/inbox/comments. | [optional] 
**AccountId** | **string** | Social account ID (ads SocialAccount). | 
**LastUpdated** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

