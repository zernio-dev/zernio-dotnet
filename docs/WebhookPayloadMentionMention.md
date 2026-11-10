# Zernio.Model.WebhookPayloadMentionMention

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Mention ID, the same as &#x60;id&#x60; on GET /v1/inbox/mentions. | 
**Platform** | **string** |  | 
**Type** | **string** | Null on LinkedIn. | 
**MediaId** | **string** | Instagram media ID. | 
**PostId** | **string** | Facebook post ID. | 
**CommentId** | **string** |  | 
**Content** | **string** | Text that mentioned the account. | 
**Permalink** | **string** | URL to the source post on LinkedIn. Null on Instagram and Facebook. | 
**AuthorUrn** | **string** |  | 
**AuthorName** | **string** |  | 
**AuthorUsername** | **string** |  | 
**AuthorPicture** | **string** |  | 
**OrganizationalEntity** | **string** | The mentioned organization, Page or Instagram account. | 
**PublishedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

