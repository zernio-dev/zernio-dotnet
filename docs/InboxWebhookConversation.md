# Zernio.Model.InboxWebhookConversation
The conversation context included in inbox webhook payloads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**PlatformConversationId** | **string** |  | 
**ParticipantId** | **string** |  | [optional] 
**ParticipantName** | **string** |  | [optional] 
**ParticipantUsername** | **string** |  | [optional] 
**ParticipantPicture** | **string** |  | [optional] 
**Status** | **string** |  | 
**ContactId** | **string** | Zernio CRM Contact ID for the participant, when one exists. Resolved by joining &#x60;participantId&#x60; to the ContactChannel collection. Best-effort: omitted when no channel matches or &#x60;participantId&#x60; is absent. Lets integrators join any inbox webhook back to the CRM Contact without needing to look at the sender — which matters for outgoing and delivery-status events whose sender is the business.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

