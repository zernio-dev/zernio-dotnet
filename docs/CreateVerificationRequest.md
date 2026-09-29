# Zernio.Model.CreateVerificationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Channel** | **string** |  | 
**To** | **string** | E.164 phone number. WhatsApp only delivers to a phone number, never to a username. | 
**From** | **string** | The number on your account to send from: an SMS-enabled number for &#x60;sms&#x60;, a connected WhatsApp number for &#x60;whatsapp&#x60;. Defaults to your only number on that channel. | [optional] 
**BrandName** | **string** | Your app or business name, rendered in the SMS message. Defaults to your account name. Not shown on WhatsApp, where Meta fixes the message and shows your WhatsApp display name. Letters, numbers, and basic punctuation only. | [optional] 
**CodeLength** | **int** |  | [optional] [default to 6]
**TtlMinutes** | **int** |  | [optional] [default to 10]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

