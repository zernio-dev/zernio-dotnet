# Zernio.Model.ScheduledEmail
An email sent with `scheduledFor`. `status` moves scheduled, sending, then sent or failed; a cancelled one never leaves.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The &#x60;scheduleId&#x60;. | [optional] 
**AccountId** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**ScheduledFor** | **DateTime** |  | [optional] 
**HoldAsDraft** | **bool** | True when the email waits as a draft in the mailbox and is sent as that draft stands at &#x60;scheduledFor&#x60;. | [optional] 
**DraftId** | **string** | The mailbox draft of a &#x60;holdAsDraft&#x60; send: the Gmail draft id, or the Outlook message id. &#x60;null&#x60; otherwise. | [optional] 
**To** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Subject** | **string** | Empty on a reply that keeps the thread subject. &#x60;null&#x60; once the send finishes under zero content retention. | [optional] 
**ContentNotRetained** | **bool** | Present and &#x60;true&#x60; when the email content was dropped under [zero content retention](/security/zero-content-retention). | [optional] 
**ReplyToMessageId** | **string** | Set when scheduled through the reply route. | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**SentAt** | **DateTime?** |  | [optional] 
**SentMessageId** | **string** | Provider id of the sent message once &#x60;status&#x60; is sent. | [optional] 
**SentThreadId** | **string** |  | [optional] 
**Error** | **string** | Why a failed send did not leave. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

