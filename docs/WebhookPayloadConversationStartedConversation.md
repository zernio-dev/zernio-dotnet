# Zernio.Model.WebhookPayloadConversationStartedConversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Internal conversation ID | 
**Platform** | **string** |  | 
**PlatformConversationId** | **string** |  | 
**ParticipantId** | **string** | Contact&#39;s platform identifier (IGSID | [optional] 
**ParticipantName** | **string** |  | 
**ParticipantUsername** | **string** | Contact&#39;s handle when the platform exposes one | [optional] 
**ParticipantPicture** | **string** |  | [optional] 
**Status** | **string** |  | 
**ContactId** | **string** | Zernio CRM Contact ID for the participant, when one exists. Resolved by joining &#x60;participantId&#x60; to the ContactChannel collection (same join used by message.*, reaction.received, and call.* webhooks). Best-effort: omitted when no channel matches or &#x60;participantId&#x60; is absent. Lets integrators seed the CRM straight from &#x60;conversation.started&#x60; without waiting for the first &#x60;message.*&#x60; event.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

