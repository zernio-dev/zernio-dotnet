# Zernio.Model.SetConversationThreadControlRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Social account ID | 
**Action** | **string** | &#x60;request&#x60; is Facebook and Instagram only. &#x60;take&#x60; and &#x60;request&#x60; are refused with &#x60;platform_not_supported&#x60; on Instagram accounts connected with Instagram Login. | 
**Target** | **string** | WhatsApp only. With action pass: send control to Meta Business Agent instead of the escalation partner. | [optional] 
**TargetAppId** | **string** | Facebook and Instagram only, required with action pass: the Meta app id receiving the thread. | [optional] 
**Metadata** | **string** | Free-form note forwarded verbatim to the app receiving control (its messaging_handovers webhook). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

