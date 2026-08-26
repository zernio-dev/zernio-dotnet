# Zernio.Model.WebhookPayloadMessageMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Internal message ID | 
**ConversationId** | **string** | Internal conversation ID | 
**Platform** | **string** |  | 
**PlatformMessageId** | **string** | Platform&#39;s message ID | 
**Direction** | **string** |  | 
**Text** | **string** | Message text content | 
**Attachments** | [**List&lt;WebhookPayloadMessageMessageAttachmentsInner&gt;**](WebhookPayloadMessageMessageAttachmentsInner.md) |  | 
**Sender** | [**WebhookPayloadMessageMessageSender**](WebhookPayloadMessageMessageSender.md) |  | 
**SentAt** | **DateTime** | When the message was sent, as reported by the platform and passed through unmodified. Full ISO 8601 date-time: Instagram and Facebook carry millisecond precision, while some platforms (for example WhatsApp and Telegram) report whole seconds. Use this field as the chronological ordering key. If two messages share the same value, fetch the conversation messages with sortOrder&#x3D;desc for the deterministic order. | 
**IsRead** | **bool** |  | 
**SentVia** | **string** | Which Zernio surface produced the message. Always present and always &#x60;null&#x60; on this event, since nobody on our side produced an inbound message; it is only informative on &#x60;message.sent&#x60;, which documents the vocabulary.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

