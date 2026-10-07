# Zernio.Model.DialVoiceWebCallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**To** | **string** | The number to call, E.164 with leading +. | 
**CredentialId** | **string** | The WebRTC credential id returned by POST /v1/voice/calls/web (the registered browser). | 
**FromNumber** | **string** | Which of your voice-enabled numbers to call from (optional when you have one). | [optional] 
**RecordOverride** | **bool** |  | [optional] 
**RingTimeoutSeconds** | **int** | Seconds to let the callee&#39;s phone ring before the call ends as no_answer. The destination carrier can end it sooner. | [optional] [default to 30]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

