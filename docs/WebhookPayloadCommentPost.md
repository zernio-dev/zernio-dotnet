# Zernio.Model.WebhookPayloadCommentPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Internal post ID (null for posts not published through Zernio) | 
**PlatformPostId** | **string** | Platform&#39;s post ID | 
**Content** | **string** | Post text, from our synced copy — no platform call is made on the comment path, so null when the post was never synced. | 
**ImageUrl** | **string** | Post thumbnail or first media item URL. Platform CDN URLs expire, fetch promptly. | 
**Permalink** | **string** | Public URL of the post. Null for posts published through Zernio that were never re-synced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

