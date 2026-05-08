# Zernio.Model.WebhookPayloadMessageMetadataStoryReply
Instagram only. Populated when an IG user replies to one of the account's stories (Meta `messaging_story_replies`). Mutually exclusive in practice with `isStoryMention`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StoryId** | **string** | The Instagram story ID the user replied to. | 
**StoryUrl** | **string** | Meta CDN URL for the story media. Expires approximately 24 hours after the story posted; consumers must fetch promptly or treat 404s as expected.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

