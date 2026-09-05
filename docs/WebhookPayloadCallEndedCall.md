# Zernio.Model.WebhookPayloadCallEndedCall

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**MetaCallId** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**PhoneNumberId** | **string** |  | [optional] 
**Direction** | **string** |  | [optional] 
**From** | **string** |  | [optional] 
**To** | **string** |  | [optional] 
**StartedAt** | **DateTime** |  | [optional] 
**EndedAt** | **DateTime** |  | [optional] 
**DurationSeconds** | **int** |  | [optional] 
**EndReason** | **string** |  | [optional] 
**HangupCause** | **string** | Raw carrier hangup cause behind endReason (e.g. normal_clearing, call_rejected, not_found). Null when the carrier reported none. | [optional] 
**SipHangupCause** | **string** | SIP response code that ended the call when SIP-signalled (e.g. &#39;403&#39;, &#39;486&#39;, &#39;603&#39;). endReason collapses all three to &#39;rejected&#39;, so this is what separates a refused destination from a busy line. Null on non-SIP legs. | [optional] 
**IsVoicemail** | **bool** | True when the inbound call was handled by voicemail, whether scheduled or because the forward did not connect. | [optional] 
**CallErrors** | [**List&lt;CallRecordCallErrorsInner&gt;**](CallRecordCallErrorsInner.md) | Failures recorded on the call up to hangup (bridge failed, dial failed, recording error). Empty on a clean call. &#x60;message&#x60; is free-form diagnostic text and is not stable, do not parse it. &#x60;code&#x60; is 0 unless a provider code is known. Errors the carrier reports after hangup appear only on GET /v1/calls/{id}. | [optional] 
**RecordingUrl** | **string** |  | [optional] 
**RecordingExpiresAt** | **DateTime** |  | [optional] 
**Billing** | [**WebhookPayloadCallEndedCallBilling**](WebhookPayloadCallEndedCallBilling.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

