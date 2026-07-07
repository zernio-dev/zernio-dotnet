# Zernio.Model.ListInboxMentions200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Mention document ID | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**Content** | **string** | Text of the post that mentioned you | [optional] 
**Permalink** | **string** | URL to the source post on LinkedIn | [optional] 
**AuthorUrn** | **string** | LinkedIn URN of the person who mentioned you | [optional] 
**AuthorName** | **string** | Display name of the author, resolved from authorUrn. Null when LinkedIn does not allow resolving the profile. | [optional] 
**AuthorUsername** | **string** | LinkedIn vanity name of the author (the slug in their profile URL) | [optional] 
**AuthorPicture** | **string** | Profile picture URL of the author. LinkedIn CDN URLs expire after some time, so fetch promptly rather than storing long-term. | [optional] 
**OrganizationalEntity** | **string** | URN of the organization that was mentioned | [optional] 
**PublishedAt** | **DateTime** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

