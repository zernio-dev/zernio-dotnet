# Zernio.Model.EmailDraft
A draft in the mailbox. Carries the message fields; `id` is the draft id the drafts endpoints take. Store `id`, not `messageId`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The draft id: the Gmail draft id, or the Outlook message id. | [optional] 
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
**Labels** | **List&lt;string&gt;** | Gmail: the ids of the user labels on the message (names come from &#x60;GET /v1/email/labels&#x60;). Outlook: its category names. | [optional] 
**Metadata** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**TrackingId** | **string** | Set when the draft was created with tracking. | [optional] 
**Clean** | [**EmailClean**](EmailClean.md) |  | [optional] 
**DraftId** | **string** | On a mail sent from a draft (&#x60;POST /v1/email/drafts/{draftId}/send&#x60;): the draft it was. The sent mail has a new id. | [optional] 
**ForwardedFrom** | **string** | On a forward: the message it forwarded. | [optional] 
**Object** | **string** |  | [optional] 
**Kind** | **string** | Fixed when the draft is created. A draft the user wrote in their mail client is read from its headers. | [optional] 
**VarVersion** | **string** | Changes on every edit, the user&#39;s in Gmail or Outlook included. Pass it as &#x60;If-Match&#x60; to update or send only that version. Also the &#x60;ETag&#x60; response header. | [optional] 
**MessageId** | **string** | The provider message behind the draft. Volatile: Gmail replaces it on every save. | [optional] 
**InReplyTo** | **string** | The message a reply draft answers. | [optional] 
**ForwardOf** | **string** | The message a forward draft forwards. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

