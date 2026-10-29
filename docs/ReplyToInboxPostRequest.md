# Zernio.Model.ReplyToInboxPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**Message** | **string** | Reply text. On LinkedIn, mention with @[Name](urn:li:person:ID) or @[Org](urn:li:organization:ID); the name must match LinkedIn&#39;s exactly (case-sensitive) or it renders as plain text. The profile-URL form is not resolved in comments, and an unknown person URN posts the plain name. | 
**AttachmentUrl** | **string** | (Facebook only) URL of an image to attach, publishing a photo comment alongside the text. The URL must be publicly accessible so Meta can fetch it. Returns 400 for other platforms. | [optional] 
**CommentId** | **string** | Reply to specific comment (optional) | [optional] 
**ParentCid** | **string** | (Bluesky only) Parent content identifier | [optional] 
**RootUri** | **string** | (Bluesky only) Root post URI | [optional] 
**RootCid** | **string** | (Bluesky only) Root post CID | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

