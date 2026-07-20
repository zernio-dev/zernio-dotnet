# Zernio.Model.ReplyToInboxPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**Message** | **string** |  | 
**AttachmentUrl** | **string** | (Facebook only) URL of an image to attach, publishing a photo comment alongside the text. The URL must be publicly accessible so Meta can fetch it. Returns 400 for other platforms. | [optional] 
**CommentId** | **string** | Reply to specific comment (optional) | [optional] 
**ParentCid** | **string** | (Bluesky only) Parent content identifier | [optional] 
**RootUri** | **string** | (Bluesky only) Root post URI | [optional] 
**RootCid** | **string** | (Bluesky only) Root post CID | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

