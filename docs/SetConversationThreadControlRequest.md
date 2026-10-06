# Zernio.Model.SetConversationThreadControlRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Social account ID | 
**Action** | **string** | &#x60;request&#x60; is Facebook and Instagram only. | 
**Target** | **string** | WhatsApp only. With action pass: send control to Meta Business Agent instead of the escalation partner. | [optional] 
**TargetAppId** | **string** | Facebook and Instagram only, required with action pass: the Meta app id receiving the thread. | [optional] 
**Metadata** | **string** | Free-form note forwarded verbatim to the app receiving control (its messaging_handovers webhook). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

