# Zernio.Model.GetInboxConversationMessages200ResponseMessagesInnerStoryReply
Instagram only. Present when the message replies to one of the account's stories. Also set on history imported after connecting, read off Meta's `story.reply_to`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StoryId** | **string** | The Instagram story ID the user replied to. | [optional] 
**StoryUrl** | **string** | Meta CDN URL for the story media. Expires roughly 24 hours after the story posted; fetch promptly or treat 404s as expected. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

