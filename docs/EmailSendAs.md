# Zernio.Model.EmailSendAs
An address the mailbox can send from.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**ReplyTo** | **string** | Gmail alias reply-to address, if set. | [optional] 
**IsPrimary** | **bool** | The mailbox&#39;s own address. | [optional] 
**IsDefault** | **bool** | The address Gmail picks by default in its compose window. | [optional] 
**Verified** | **bool** | Gmail sends from an alias only once it is verified. Always &#x60;true&#x60; on Outlook. | [optional] 
**Signature** | **string** | Signature html. Gmail only; always &#x60;null&#x60; on Outlook. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

