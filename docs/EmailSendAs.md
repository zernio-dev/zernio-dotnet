# Zernio.Model.EmailSendAs
An address the mailbox can send from: listed by the provider, or declared with `POST /v1/email/send-as`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **string** |  | [optional] 
**Name** | **string** | Display name used when &#x60;fromName&#x60; is not given. | [optional] 
**Type** | **string** | &#x60;primary&#x60; is the mailbox&#39;s own address, &#x60;alias&#x60; a provider alias, &#x60;shared&#x60; a declared address (shared mailbox, delegate or alias). | [optional] 
**VerificationStatus** | **string** | &#x60;pending&#x60;: Gmail has not verified the alias, so sends from it are refused. &#x60;unverified&#x60;: declared and not sent from yet; it becomes &#x60;accepted&#x60; after its first send. | [optional] 
**IsDefault** | **bool** | The address the provider picks by default. | [optional] 
**Source** | **string** |  | [optional] 
**ReplyTo** | **string** | Gmail alias reply-to address, if set. | [optional] 
**Signature** | [**EmailSendAsSignature**](EmailSendAsSignature.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

