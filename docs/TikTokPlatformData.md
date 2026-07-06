# Zernio.Model.TikTokPlatformData
Photo carousels up to 35 images. Video titles up to 2200 chars, photo titles truncated to 90 chars. privacyLevel must match creator_info options. Both camelCase and snake_case accepted.  Creator Inbox (draft mode): Set draft: true to send content to the TikTok Creator Inbox instead of publishing immediately. The creator receives an inbox notification and completes the post using TikTok's editing flow. This maps to TikTok's post_mode: \"MEDIA_UPLOAD\" internally.  Important: The field publish_type is NOT supported. Use draft: true for Creator Inbox flow.  Photo drafts use the /v2/post/publish/content/init/ endpoint with post_mode: \"MEDIA_UPLOAD\". Video drafts use the dedicated /v2/post/publish/inbox/video/init/ endpoint.  When draft: true, the video.upload scope is required. When draft is false or omitted (direct post), the video.publish scope is required. For Creator Inbox, TikTok app version must be 31.8 or higher. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Draft** | **bool** | When true, sends the post to the TikTok Creator Inbox as a draft instead of publishing immediately. The creator receives an inbox notification to complete posting via TikTok&#39;s editing flow. Maps to TikTok API post_mode: \&quot;MEDIA_UPLOAD\&quot; (photos) or the dedicated inbox endpoint (videos). When false or omitted, publishes directly via post_mode: \&quot;DIRECT_POST\&quot;. Note: publish_type is not a supported field. Use this field instead.  | [optional] 
**PrivacyLevel** | **string** | One of the values returned by the TikTok creator info API for the account | [optional] 
**AllowComment** | **bool** | Allow comments on the post | [optional] 
**AllowDuet** | **bool** | Allow duets (required for video posts) | [optional] 
**AllowStitch** | **bool** | Allow stitches (required for video posts) | [optional] 
**CommercialContentType** | **string** | Type of commercial content disclosure. Sufficient on its own: \&quot;brand_organic\&quot; (\&quot;Your Brand\&quot;) implies isBrandOrganicPost and \&quot;brand_content\&quot; (\&quot;Branded Content\&quot;, paid partnership) implies brandPartnerPromote, so you don&#39;t need to send the boolean flags separately. Branded content cannot be posted with privacyLevel SELF_ONLY.  | [optional] 
**BrandPartnerPromote** | **bool** | Whether the post promotes a brand partner (branded content / paid partnership). Only needed to disclose BOTH types at once (set it alongside commercialContentType \&quot;brand_organic\&quot;), or to override the value implied by commercialContentType.  | [optional] 
**IsBrandOrganicPost** | **bool** | Whether the post promotes the creator&#39;s own brand (brand organic). Only needed to disclose BOTH types at once (set it alongside commercialContentType \&quot;brand_content\&quot;), or to override the value implied by commercialContentType.  | [optional] 
**ContentPreviewConfirmed** | **bool** | User has confirmed they previewed the content | [optional] 
**ExpressConsentGiven** | **bool** | User has given express consent for posting | [optional] 
**MediaType** | **string** | Optional override. Defaults based on provided media items. | [optional] 
**VideoCoverTimestampMs** | **int** | Optional for video posts. Timestamp in milliseconds to select which frame to use as thumbnail (defaults to 1000ms/1 second). Ignored when videoCoverImageUrl is provided. | [optional] 
**VideoCoverImageUrl** | **string** | Optional for video posts. URL of a custom thumbnail image (JPG, PNG, or WebP, max 20MB). The image is stitched as a single frame at the start of the video and used as the cover. Overrides videoCoverTimestampMs when provided. | [optional] 
**PhotoCoverIndex** | **int** | Optional for photo carousels. Index of image to use as cover, 0-based (defaults to 0/first image). | [optional] 
**AutoAddMusic** | **bool** | When true, TikTok may add recommended music (photos only) | [optional] 
**VideoMadeWithAi** | **bool** | Set true to disclose AI-generated content | [optional] 
**Description** | **string** | Optional long-form description for photo posts (max 4000 chars). Recommended when content exceeds 90 chars, as photo titles are auto-truncated. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

