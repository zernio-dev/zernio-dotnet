# Zernio.Model.WebhookPayloadCommentCommentAttachment
Facebook only. Present on graphic-only comments (sticker, GIF, photo) that carry no text. URLs are ephemeral and may expire for Meta platforms (oe= expiry), so fetch promptly. Instagram comments do not support attachments. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Attachment type: sticker, animated_image_share, or photo. | 
**ImageUrl** | **string** | Rendered image/preview URL (from attachment.media.image.src). | [optional] 
**Url** | **string** | Source URL (from attachment.url). For GIFs this is an l.facebook.com redirect. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

