# Zernio.Model.WebhookPayloadCallReceivedCall

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Internal Zernio Call doc id | [optional] 
**MetaCallId** | **string** | Meta wacid.* call id when known | [optional] 
**AccountId** | **string** |  | [optional] 
**PhoneNumberId** | **string** | Meta phone_number_id | [optional] 
**Direction** | **string** |  | [optional] 
**From** | **string** | Consumer wa_id / E.164 | [optional] 
**To** | **string** | Business number (E.164) | [optional] 
**ForwardTo** | **string** | Destination snapshot at routing time | [optional] 
**TelnyxCallControlId** | **string** | Carrier call_control_id of this call leg. Equals start.call_control_id of the media stream a wss:// forwardTo receives. | [optional] 
**TelnyxCallSessionId** | **string** | Carrier call_session_id of this call. Equals start.call_session_id of the media stream a wss:// forwardTo receives. | [optional] 
**ContactId** | **string** |  | [optional] 
**ConversationId** | **string** |  | [optional] 
**StartedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

