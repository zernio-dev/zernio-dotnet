# Zernio.Model.CommentAutomationDmMedia
An image, video, audio clip or file sent right after the DM text as a second message (a Meta message carries one body, so text and attachment are two sends). On the comment trigger Meta may refuse the second message until the commenter replies; the DM then still counts as sent and the log row carries `mediaError`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Url** | **string** | Publicly reachable http(s) URL Meta downloads the media from. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

