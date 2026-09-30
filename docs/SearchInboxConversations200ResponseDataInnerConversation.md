# Zernio.Model.SearchInboxConversations200ResponseDataInnerConversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Conversation ID, usable with the conversation messages endpoints | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**ParticipantName** | **string** |  | [optional] 
**ParticipantUsername** | **string** |  | [optional] 
**ParticipantPicture** | **string** |  | [optional] 
**BusinessScopedUserId** | **string** | WhatsApp only. Meta business-scoped user ID (BSUID), the stable identity anchor; present when Meta has sent it for this participant. | [optional] 
**WhatsappUsername** | **string** | WhatsApp only. The participant&#39;s WhatsApp username (e.g. &#x60;jane.shop&#x60;, no leading @). Not a stable identifier, because users can change it: useful for display, not recommended as an identity anchor. Captured from inbound messages, so older threads fill in on their next inbound. | [optional] 
**Status** | **string** |  | [optional] 
**LastMessage** | **string** | The conversation&#39;s most recent message preview | [optional] 
**LastMessageAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

