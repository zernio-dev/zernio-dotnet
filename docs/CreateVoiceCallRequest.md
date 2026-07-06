# Zernio.Model.CreateVoiceCallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**To** | **string** | Destination to dial, E.164 with leading +. | 
**FromNumber** | **string** | Which of your voice-enabled numbers to dial from. Optional when you have exactly one. | [optional] 
**ForwardTo** | **string** | Per-call agent override (tel:+E164, sip:..., or wss://...); defaults to the number&#39;s stored forward destination. | [optional] 
**Greeting** | **string** | Spoken to the callee when they answer, before the bridge. | [optional] 
**RecordOverride** | **bool** | Per-call recording toggle; defaults to the number&#39;s setting. | [optional] 
**TranscribeOverride** | **bool** | Per-call transcription toggle; defaults to the number&#39;s setting. | [optional] 
**TranscriptionLanguage** | **string** | &#39;auto&#39; derives from the callee&#39;s country; &#39;en&#39;/&#39;es&#39; force it. | [optional] 
**Amd** | **bool** | Answering-machine detection; defers the bridge until human vs machine is known. | [optional] 
**VoicemailDropMessage** | **string** | Spoken to a detected machine, then hang up (implies &#x60;amd&#x60;). For outbound voicemail drops. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

