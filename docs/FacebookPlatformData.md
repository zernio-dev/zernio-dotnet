# Zernio.Model.FacebookPlatformData
Facebook post settings.  - Feed posts: up to 10 images (no mixed video+image). - Stories: single media (24h, no captions). - Reels: a single vertical video (9:16). The Zernio API does not preflight Reel duration; Meta's Reels publishing guide documents 3-90 seconds. - Geo-restriction: a hard visibility restriction (users outside the specified countries cannot see the post). Not supported for stories.  Draft, carousel and colored-background text options live under facebookSettings, see FacebookSettings. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContentType** | **string** | Set to &#39;story&#39; for Page Stories (24h ephemeral) or &#39;reel&#39; for Reels (short vertical video). Defaults to feed post if omitted. | [optional] 
**Title** | **string** | Reel title (only for contentType&#x3D;reel). Separate from the caption/content field. | [optional] 
**FirstComment** | **string** | Optional first comment to post immediately after publishing (feed posts and reels, not stories). Skipped when facebookSettings.draft is true. | [optional] 
**IsAiGenerated** | **bool** | When true, Facebook shows its AI-disclosure label on the post. Forwarded as is_ai_generated on Reels (contentType&#x3D;reel) and video Stories (contentType&#x3D;story with a video). Meta documents no such parameter for feed posts, feed videos or photo Stories, so the flag is accepted with a warning and no label there. | [optional] [default to false]
**PageId** | **string** | Target Facebook Page ID for multi-page posting. If omitted, uses the default page. Use GET /v1/accounts/{id}/facebook-page to list pages. | [optional] 
**GeoRestriction** | [**GeoRestriction**](GeoRestriction.md) |  | [optional] 
**Collaborators** | **List&lt;string&gt;** | Facebook Page IDs (numeric, up to 10 unique) to invite as collaborators. Reels only (contentType&#x3D;reel), sent after the Reel is published, never for drafts. Each Page must accept. Meta allows 10 invites per Page per 24 hours; rejected invites are listed in failedCollaborators. Other values are ignored with a warning. | [optional] 
**FailedCollaborators** | [**List&lt;FacebookPlatformDataFailedCollaboratorsInner&gt;**](FacebookPlatformDataFailedCollaboratorsInner.md) | Output only. Collaborator invites Facebook rejected after the Reel was published. The Reel itself stays published. | [optional] 
**FacebookSettings** | [**FacebookSettings**](FacebookSettings.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

