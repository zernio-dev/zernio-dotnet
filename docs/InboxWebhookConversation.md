# Zernio.Model.InboxWebhookConversation
The conversation context included in inbox webhook payloads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Zernio&#39;s internal conversation id (also the message&#39;s conversationId). Accepted by every /v1/inbox/conversations/{conversationId} endpoint. | 
**PlatformConversationId** | **string** | The platform&#39;s conversation id. This is the &#x60;id&#x60; GET /v1/inbox/conversations returns for the same conversation (on Instagram and Messenger it is the participant&#39;s IGSID / PSID), so key your records on it to match webhooks with list rows. Also accepted by the conversation endpoints. | 
**ParticipantId** | **string** |  | [optional] 
**ParticipantName** | **string** |  | [optional] 
**ParticipantUsername** | **string** |  | [optional] 
**ParticipantPicture** | **string** |  | [optional] 
**Status** | **string** |  | 
**ContactId** | **string** | Zernio CRM Contact ID for the participant, when one exists. Resolved by joining &#x60;participantId&#x60; to the ContactChannel collection. Best-effort: omitted when no channel matches or &#x60;participantId&#x60; is absent. Lets integrators join any inbox webhook back to the CRM Contact without needing to look at the sender, which matters for outgoing and delivery-status events whose sender is the business.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

