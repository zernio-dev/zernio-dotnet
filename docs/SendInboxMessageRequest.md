# Zernio.Model.SendInboxMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Social account ID | 
**Message** | **string** | Message text | [optional] 
**AttachmentUrl** | **string** | URL of the attachment to send (image, video, audio, or file). The URL must be publicly accessible. For binary file uploads, use multipart/form-data instead. | [optional] 
**AttachmentType** | **string** | Type of attachment. Defaults to file if not specified. | [optional] 
**AttachmentName** | **string** | WhatsApp only. Display name for a document sent via attachmentUrl with attachmentType: file (e.g. \&quot;Report.pdf\&quot;). Maps to the recipient&#39;s file name; without it WhatsApp derives the name from the URL and shows \&quot;Untitled\&quot;. Ignored for image/video/audio and for binary uploads (which use the uploaded file&#39;s name). | [optional] 
**VoiceNote** | **bool** | WhatsApp only. When &#x60;true&#x60; on an audio attachment, the message is sent as a voice message (PTT) — the recipient sees the waveform + voice-note UI instead of a basic audio attachment. The audio file MUST be &#x60;.ogg&#x60; encoded with the OPUS codec (mono) per Meta&#39;s voice-message contract; other formats are rejected by WhatsApp. Ignored for non-audio attachments.  | [optional] 
**QuickReplies** | [**List&lt;SendInboxMessageRequestQuickRepliesInner&gt;**](SendInboxMessageRequestQuickRepliesInner.md) | Quick reply buttons. Mutually exclusive with buttons. Max 13 items. | [optional] 
**Buttons** | [**List&lt;SendInboxMessageRequestButtonsInner&gt;**](SendInboxMessageRequestButtonsInner.md) | Action buttons. Mutually exclusive with quickReplies. Max 3 items.  WhatsApp: buttons always render as interactive reply buttons. Only &#x60;title&#x60; and &#x60;payload&#x60; are used — &#x60;type&#x60;, &#x60;url&#x60;, and &#x60;phone&#x60; are ignored (WhatsApp has no URL/phone button in this field; use the &#x60;interactive&#x60; field with &#x60;type: cta_url&#x60; for a link button). &#x60;payload&#x60; becomes the button reply ID delivered on the &#x60;message.received&#x60; webhook when the user taps. To send a simple reply-button message, provide &#x60;title&#x60; + &#x60;payload&#x60; and set &#x60;type: postback&#x60;, e.g. &#x60;{ \&quot;type\&quot;: \&quot;postback\&quot;, \&quot;title\&quot;: \&quot;Yes\&quot;, \&quot;payload\&quot;: \&quot;yes\&quot; }&#x60;.  | [optional] 
**Template** | [**SendInboxMessageRequestTemplate**](SendInboxMessageRequestTemplate.md) |  | [optional] 
**Interactive** | [**SendInboxMessageRequestInteractive**](SendInboxMessageRequestInteractive.md) |  | [optional] 
**ReplyMarkup** | [**SendInboxMessageRequestReplyMarkup**](SendInboxMessageRequestReplyMarkup.md) |  | [optional] 
**MessagingType** | **string** | Facebook messaging type. Required when using messageTag. | [optional] 
**MessageTag** | **string** | Facebook message tag for messaging outside 24h window. Requires messagingType MESSAGE_TAG. Instagram only supports HUMAN_AGENT. | [optional] 
**ReplyTo** | **string** | Platform message ID to quote-reply to. For WhatsApp, pass the wamid (available in message.platformMessageId from webhooks). For Telegram, pass the Telegram message ID. | [optional] 
**Location** | [**SendInboxMessageRequestLocation**](SendInboxMessageRequestLocation.md) |  | [optional] 
**Contacts** | [**List&lt;SendInboxMessageRequestContactsInner&gt;**](SendInboxMessageRequestContactsInner.md) | WhatsApp-only. Send one or more contact cards. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

