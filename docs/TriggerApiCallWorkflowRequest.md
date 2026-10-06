# Zernio.Model.TriggerApiCallWorkflowRequest
Exactly one of `conversationId`, `contactId` or `to`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConversationId** | **string** | A conversation on the workflow&#39;s account | [optional] 
**ContactId** | **string** | A contact with a conversation on the workflow&#39;s account | [optional] 
**To** | **string** | Recipient phone in E.164 (WhatsApp workflows only) | [optional] 
**Variables** | **Dictionary&lt;string, Object&gt;** | Seed variables, merged over the standard run variables | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

