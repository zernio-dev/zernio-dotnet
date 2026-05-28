# Zernio.Model.SendInboxMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Social account ID | 
**Message** | **string** | Message text | [optional] 
**AttachmentUrl** | **string** | URL of the attachment to send (image, video, audio, or file). The URL must be publicly accessible. For binary file uploads, use multipart/form-data instead. | [optional] 
**AttachmentType** | **string** | Type of attachment. Defaults to file if not specified. | [optional] 
**VoiceNote** | **bool** | WhatsApp only. When &#x60;true&#x60; on an audio attachment, the message is sent as a voice message (PTT) — the recipient sees the waveform + voice-note UI instead of a basic audio attachment. The audio file MUST be &#x60;.ogg&#x60; encoded with the OPUS codec (mono) per Meta&#39;s voice-message contract; other formats are rejected by WhatsApp. Ignored for non-audio attachments.  | [optional] 
**QuickReplies** | [**List&lt;SendInboxMessageRequestQuickRepliesInner&gt;**](SendInboxMessageRequestQuickRepliesInner.md) | Quick reply buttons. Mutually exclusive with buttons. Max 13 items. | [optional] 
**Buttons** | [**List&lt;SendInboxMessageRequestButtonsInner&gt;**](SendInboxMessageRequestButtonsInner.md) | Action buttons. Mutually exclusive with quickReplies. Max 3 items. | [optional] 
**Template** | [**SendInboxMessageRequestTemplate**](SendInboxMessageRequestTemplate.md) |  | [optional] 
**Interactive** | [**SendInboxMessageRequestInteractive**](SendInboxMessageRequestInteractive.md) |  | [optional] 
**ReplyMarkup** | [**SendInboxMessageRequestReplyMarkup**](SendInboxMessageRequestReplyMarkup.md) |  | [optional] 
**MessagingType** | **string** | Facebook messaging type. Required when using messageTag. | [optional] 
**MessageTag** | **string** | Facebook message tag for messaging outside 24h window. Requires messagingType MESSAGE_TAG. Instagram only supports HUMAN_AGENT. | [optional] 
**ReplyTo** | **string** | Platform message ID to quote-reply to. For WhatsApp, pass the wamid (available in message.platformMessageId from webhooks). For Telegram, pass the Telegram message ID. | [optional] 
**Location** | [**SendInboxMessageRequestLocation**](SendInboxMessageRequestLocation.md) |  | [optional] 
**Contacts** | [**List&lt;SendInboxMessageRequestContactsInner&gt;**](SendInboxMessageRequestContactsInner.md) | WhatsApp-only. Send one or more contact cards. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

