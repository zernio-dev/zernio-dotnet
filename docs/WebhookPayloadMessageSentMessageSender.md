# Zernio.Model.WebhookPayloadMessageSentMessageSender
**On this event the sender is your own business, not the person you are talking to.** `id` is the Zernio account id and `name`, `username` and `picture` are that connected account's own profile.  Do not read these to name or update a contact: doing so on an echo relabels the customer's record with your business name. The other party is `conversation.participantId` / `participantName` / `participantUsername`.  `participantId` is always set. On a thread the business started, `participantUsername` and `participantName` can be empty on the first events; Zernio fills them shortly after when Meta returns the contact (`participantName` then holds the @username until the contact writes and their profile is read). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The Zernio account id of the connected account that sent the message, not a contact id. | 
**ContactId** | **string** | Always omitted on this event: the sender is the business, not a contact. Use conversation.contactId to join back to the CRM Contact. | [optional] 
**Name** | **string** | Display name of your connected account. | [optional] 
**Username** | **string** | Username of your connected account. | [optional] 
**Picture** | **string** | Profile picture of your connected account. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

