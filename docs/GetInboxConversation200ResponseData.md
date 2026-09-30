# Zernio.Model.GetInboxConversation200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**ParticipantName** | **string** |  | [optional] 
**ParticipantId** | **string** |  | [optional] 
**ParticipantVerifiedType** | **string** | X verified badge type. Only present for X conversations. | [optional] 
**BusinessScopedUserId** | **string** | WhatsApp only. Meta business-scoped user ID (BSUID), the stable identity anchor; present when Meta has sent it for this participant. | [optional] 
**WhatsappUsername** | **string** | WhatsApp only. The participant&#39;s WhatsApp username (e.g. &#x60;jane.shop&#x60;, no leading @). Not a stable identifier, because users can change it: useful for display, not recommended as an identity anchor. Captured from inbound messages, so older threads fill in on their next inbound. | [optional] 
**LastMessage** | **string** |  | [optional] 
**LastMessageAt** | **DateTime** |  | [optional] 
**UpdatedTime** | **DateTime** |  | [optional] 
**Participants** | [**List&lt;UpdateFacebookPage200ResponseSelectedPage&gt;**](UpdateFacebookPage200ResponseSelectedPage.md) |  | [optional] 
**InstagramProfile** | [**ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md) |  | [optional] 
**Metadata** | [**GetInboxConversation200ResponseDataMetadata**](GetInboxConversation200ResponseDataMetadata.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

