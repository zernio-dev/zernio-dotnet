# Zernio.Model.CreateVerificationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Channel** | **string** | SMS-only for now. | 
**To** | **string** | E.164 phone number. | 
**From** | **string** | The SMS-enabled number on your account to send from. Defaults to your only SMS number. | [optional] 
**BrandName** | **string** | Your app or business name, rendered in the message. Defaults to your account name. Letters, numbers, and basic punctuation only. | [optional] 
**CodeLength** | **int** |  | [optional] [default to 6]
**TtlMinutes** | **int** |  | [optional] [default to 10]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

