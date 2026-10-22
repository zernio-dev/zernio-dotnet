# Zernio.Model.ListInboxMentions200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Mention document ID | [optional] 
**Platform** | **string** |  | [optional] 
**Type** | **string** | Instagram only: &#x60;caption&#x60; when the account was tagged in a media caption, &#x60;comment&#x60; when it was tagged in a comment. Null for LinkedIn. | [optional] 
**MediaId** | **string** | Instagram only: ID of the media the account was mentioned in (or under). Null for LinkedIn. | [optional] 
**CommentId** | **string** | Instagram only: ID of the comment that mentioned the account. Null for caption mentions and LinkedIn. | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**Content** | **string** | Text that mentioned you: the post text on LinkedIn, the caption or comment text on Instagram. Empty until it has been read. | [optional] 
**Permalink** | **string** | URL to the source post on LinkedIn. Null on Instagram. | [optional] 
**AuthorUrn** | **string** | LinkedIn URN of the person who mentioned you, or the Instagram-scoped ID of the commenter on an Instagram comment mention. | [optional] 
**AuthorName** | **string** | Display name of the author, resolved from authorUrn. Null when LinkedIn does not allow resolving the profile. | [optional] 
**AuthorUsername** | **string** | LinkedIn vanity name of the author (the slug in their profile URL), or the Instagram username of the commenter or media owner. | [optional] 
**AuthorPicture** | **string** | Profile picture URL of the author. LinkedIn CDN URLs expire after some time, so fetch promptly rather than storing long-term. | [optional] 
**OrganizationalEntity** | **string** | URN of the LinkedIn organization that was mentioned, or the Instagram user ID of the mentioned account. | [optional] 
**PublishedAt** | **DateTime** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

