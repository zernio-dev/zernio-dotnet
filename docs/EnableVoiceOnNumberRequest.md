# Zernio.Model.EnableVoiceOnNumberRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ForwardTo** | **string** | tel:+E164, sip:..., or wss://... destination for inbound calls. Empty string clears the forward (outbound-only); omitted preserves the current one. | [optional] 
**RecordingEnabled** | **bool** |  | [optional] 
**TranscriptionEnabled** | **bool** |  | [optional] 
**TranscriptionLanguage** | **string** |  | [optional] 
**VoicemailEnabled** | **bool** | Voicemail is taken when there&#39;s no live destination. Default on. | [optional] 
**VoicemailGreeting** | **string** | Custom spoken greeting; empty string restores the default. | [optional] 
**BusinessHoursEnabled** | **bool** | Outside the windows, inbound skips the forward and goes to voicemail. Off &#x3D; 24/7. | [optional] 
**BusinessHoursTimezone** | **string** | IANA timezone the windows are evaluated in. | [optional] 
**BusinessHours** | [**List&lt;EnableVoiceOnNumberRequestBusinessHoursInner&gt;**](EnableVoiceOnNumberRequestBusinessHoursInner.md) |  | [optional] 
**BlockedCallers** | **List&lt;string&gt;** | E.164 numbers rejected before answer. Replaces the whole list; bare 10-digit values are normalized as US numbers. | [optional] 
**ForwardCallerId** | **string** | Caller ID on the forwarded leg: your number (&#x60;business&#x60;) or the original caller&#39;s (&#x60;caller&#x60;). | [optional] 
**IvrEnabled** | **bool** | IVR menu (supersedes the plain forward within business hours). | [optional] 
**IvrPrompt** | **string** |  | [optional] 
**IvrOptions** | [**List&lt;EnableVoiceOnNumberRequestIvrOptionsInner&gt;**](EnableVoiceOnNumberRequestIvrOptionsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

