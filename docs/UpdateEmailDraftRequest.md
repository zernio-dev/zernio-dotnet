# Zernio.Model.UpdateEmailDraftRequest
Every field is optional; the ones you leave out keep their current value. `text` or `html` replaces the whole body, and `attachments` replaces the whole set.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**To** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Cc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Bcc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**ReplyTo** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Subject** | **string** |  | [optional] 
**Text** | **string** |  | [optional] 
**Html** | **string** | On a draft created with tracking, the new html is instrumented again under the same &#x60;trackingId&#x60;. | [optional] 
**Attachments** | [**List&lt;EmailAttachmentInput&gt;**](EmailAttachmentInput.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

