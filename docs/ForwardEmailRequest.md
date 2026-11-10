# Zernio.Model.ForwardEmailRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**To** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | 
**Cc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Bcc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**ReplyTo** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**FromName** | **string** |  | [optional] 
**From** | **string** | Send from another address of the mailbox, as on &#x60;POST /v1/email/messages&#x60;. | [optional] 
**AppendSignature** | **bool** | Appends the signature of the sending address to the note, above the forwarded original: its Zernio default first, else its Gmail signature. | [optional] 
**SignatureId** | **string** | Appends this Zernio signature to the note instead. Wins over &#x60;appendSignature&#x60;. | [optional] 
**Subject** | **string** | Defaults to \&quot;Fwd: \&quot; plus the original subject. | [optional] 
**Text** | **string** | Optional note above the forwarded mail. | [optional] 
**Html** | **string** | Optional note above the forwarded mail, as html. | [optional] 
**Attachments** | [**List&lt;EmailAttachmentInput&gt;**](EmailAttachmentInput.md) | Added to the forwarded attachments. Everything together stays under 25 MB, else 413 &#x60;attachment_too_large&#x60;. | [optional] 
**IncludeAttachments** | **bool** | False keeps only the inline images of the original. | [optional] [default to true]
**ExcludeAttachmentIds** | **List&lt;string&gt;** | Attachment ids (from a read of the original) to leave out. | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**TrackOpens** | **bool** | Adds an open pixel to the note and fires &#x60;email.opened&#x60;. Needs &#x60;html&#x60;. | [optional] 
**TrackLinks** | **bool** | Rewrites the links of the note and fires &#x60;email.link_clicked&#x60;. Needs &#x60;html&#x60;. | [optional] 
**TrackReplies** | **bool** | Fires &#x60;email.thread_replied&#x60; when someone else writes in the thread. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

