# Zernio.Model.CreateInboxConversation201ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MessageId** | **string** | Platform message ID (dm_event_id) | [optional] 
**ConversationId** | **string** | Platform conversation ID (dm_conversation_id). For WhatsApp, this is Zernio&#39;s internal conversation id (24-character hex) which matches the id returned by the list-conversations endpoint and the conversationId in the message.received and conversation.started webhooks; use it to correlate the created thread with inbound events. | [optional] 
**ParticipantId** | **string** | X numeric user ID of the recipient | [optional] 
**ParticipantName** | **string** | Display name of the recipient | [optional] 
**ParticipantUsername** | **string** | X username of the recipient | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

