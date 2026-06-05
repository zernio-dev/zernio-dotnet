# Zernio.Model.WebhookPayloadExternalPost
Webhook payload for post.external.created / post.external.updated / post.external.deleted. Fired by Zernio's background sync when it detects a natively-authored post (e.g. a Google Business Profile localPost created in the Google UI), NOT a post published through Zernio. Poll-driven (~hourly), not real-time. On post.external.deleted, post.deletedAt is populated. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Post** | [**ExternalPostWebhookPost**](ExternalPostWebhookPost.md) |  | 
**Account** | [**WebhookPayloadReviewNewAccount**](WebhookPayloadReviewNewAccount.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

