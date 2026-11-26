# Zernio.Model.WebhookPayloadMessageSentMetadataTemplateHeader
WhatsApp template sends only. The header as the recipient saw it: a text header filled with the values actually sent, a media header with its format and the link the send gave, or a location header with only its format.  Absent when the template has no header, and on bulk, broadcast and automation sends, which carry only `templateName` and `templateLanguage`. The message text is the body only. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Format** | **string** | Header format. | 
**Text** | **string** | Text headers only. The header text with its variables filled in. | [optional] 
**MediaUrl** | **string** | Image, video and document headers only. The link the send carried. Absent when the media was sent by id or the link is on Meta&#39;s CDN (an expiring URL, such as the approval sample). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

