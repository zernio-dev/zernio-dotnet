# Zernio.Model.ListInboxConversations200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Opaque conversation identifier. Pass it back verbatim to any /v1/inbox/conversations/{conversationId} route; do not assume a fixed format. | [optional] 
**Platform** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**ParticipantId** | **string** |  | [optional] 
**ParticipantName** | **string** |  | [optional] 
**ParticipantPicture** | **string** |  | [optional] 
**ParticipantVerifiedType** | **string** | X verified badge type. Only present for X conversations. | [optional] 
**LastMessage** | **string** |  | [optional] 
**UpdatedTime** | **DateTime** |  | [optional] 
**Status** | **string** |  | [optional] 
**UnreadCount** | **int?** | Number of unread messages | [optional] 
**ThreadControl** | **string** | WhatsApp only, present once Meta Business Agent has touched the thread. ai_agent: the agent answers and new inbound arrive flagged metadata.standby; app: you hold control; other: another partner app does. Change it with POST /v1/inbox/conversations/{conversationId}/thread-control. | [optional] 
**Url** | **string** | Direct link to open the conversation on the platform (if available) | [optional] 
**InstagramProfile** | [**ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md) |  | [optional] 
**Metadata** | [**ListInboxConversations200ResponseDataInnerMetadata**](ListInboxConversations200ResponseDataInnerMetadata.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

