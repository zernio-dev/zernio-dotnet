# Zernio.Model.CreateInboxConversationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The social account ID to send from | 
**ParticipantId** | **string** | Recipient identifier. For X this is the numeric user ID; for WhatsApp, the recipient phone number in international format (digits, country code included). Provide either this or participantUsername. | [optional] 
**ParticipantUsername** | **string** | Recipient handle/username — an X or Bluesky handle (with or without @) or a Reddit username (with or without u/). Resolved via lookup. Provide either this or participantId. | [optional] 
**Message** | **string** | Text content of the message. At least one of message, attachment, or (for WhatsApp) templateName is required. | [optional] 
**SkipDmCheck** | **bool** | X/Twitter only. Skip the receives_your_dm eligibility check before sending. Use if you have already verified the recipient accepts DMs. | [optional] [default to false]
**TemplateName** | **string** | WhatsApp only. Name of the approved template to start the conversation with (required for WhatsApp). | [optional] 
**TemplateLanguage** | **string** | WhatsApp only. Template language code (e.g. en_US). | [optional] 
**TemplateParams** | **List&lt;string&gt;** | WhatsApp only. Body variable values, in order. Works with positional placeholders ({{1}}, {{2}}, ...) and with named placeholders ({{name}}, {{company}} - how Meta Business Manager creates templates), where values fill the named slots in order of appearance. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

