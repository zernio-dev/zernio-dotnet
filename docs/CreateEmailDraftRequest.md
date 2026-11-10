# Zernio.Model.CreateEmailDraftRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**To** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) | Optional on a draft; needed before it is sent. | [optional] 
**Cc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**Bcc** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**ReplyTo** | [**List&lt;EmailAddress&gt;**](EmailAddress.md) |  | [optional] 
**FromName** | **string** |  | [optional] 
**From** | **string** | Send from another address of the mailbox, as on &#x60;POST /v1/email/messages&#x60;. Checked when the draft is saved. | [optional] 
**AppendSignature** | **bool** | Gmail only. Puts the signature of the sending address in the draft body, where the user sees it. | [optional] 
**Subject** | **string** | On a reply draft, empty keeps the thread subject. | [optional] 
**Text** | **string** |  | [optional] 
**Html** | **string** |  | [optional] 
**Attachments** | [**List&lt;EmailAttachmentInput&gt;**](EmailAttachmentInput.md) |  | [optional] 
**Headers** | **Dictionary&lt;string, string&gt;** | Custom &#x60;X-&#x60; headers only. | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** | Kept with the draft and returned on the sent message and its email.* webhooks. | [optional] 
**InReplyTo** | **string** | Makes a reply draft in that message&#39;s thread, addressed and threaded like a reply. Not with &#x60;forwardOf&#x60;. | [optional] 
**ReplyAll** | **bool** | With &#x60;inReplyTo&#x60;: address every recipient of the original. Leave out &#x60;to&#x60;, &#x60;cc&#x60; and &#x60;bcc&#x60;. | [optional] 
**ForwardOf** | **string** | Makes a forward draft of that message, with its attachments. Recipients can come later. Not with &#x60;inReplyTo&#x60;. | [optional] 
**IncludeAttachments** | **bool** | With &#x60;forwardOf&#x60;: false keeps only the inline images of the original. | [optional] [default to true]
**ExcludeAttachmentIds** | **List&lt;string&gt;** | With &#x60;forwardOf&#x60;: attachment ids (from a read of the original) to leave out. | [optional] 
**TrackOpens** | **bool** | Puts the open pixel in the draft html now; fires &#x60;email.opened&#x60; once it is sent. Needs &#x60;html&#x60;. | [optional] 
**TrackLinks** | **bool** | Rewrites the draft&#39;s links now; fires &#x60;email.link_clicked&#x60; once it is sent. Needs &#x60;html&#x60;. | [optional] 
**TrackReplies** | **bool** | Fires &#x60;email.thread_replied&#x60; once it is sent. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

