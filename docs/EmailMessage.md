# Zernio.Model.EmailMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The provider&#39;s message id. | [optional] 
**ThreadId** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**Provider** | **string** |  | [optional] 
**Folders** | **List&lt;string&gt;** |  | [optional] 
**From** | [**EmailAddress**](EmailAddress.md) |  | [optional] 
**To** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Cc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Bcc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**ReplyTo** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Subject** | **string** |  | [optional] 
**Snippet** | **string** |  | [optional] 
**Text** | **string** |  | [optional] 
**Html** | **string** |  | [optional] 
**Attachments** | [**List&lt;EmailAttachment&gt;**](EmailAttachment.md) |  | [optional] 
**Headers** | **Dictionary&lt;string, string&gt;** | Only with &#x60;includeHeaders&#x3D;true&#x60;. | [optional] 
**Raw** | **string** | MIME source, only with &#x60;raw&#x3D;true&#x60;. | [optional] 
**Date** | **DateTime** |  | [optional] 
**Unread** | **bool** |  | [optional] 
**Starred** | **bool** |  | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

