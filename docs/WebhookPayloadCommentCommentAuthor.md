# Zernio.Model.WebhookPayloadCommentCommentAuthor

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Author&#39;s platform ID | 
**Username** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Picture** | **string** |  | [optional] 
**IsOwnAccount** | **bool** | True when this comment was authored by the connected account itself (Meta re-delivers the account&#39;s own replies as comments events). Populated on the Instagram and Facebook realtime webhooks only; absent means not evaluated, never \&quot;not the account\&quot;. | [optional] 
**InstagramProfile** | [**WebhookPayloadCommentCommentAuthorInstagramProfile**](WebhookPayloadCommentCommentAuthorInstagramProfile.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

