# Zernio.Model.CompleteWhatsAppPhoneSelectionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | The Zernio profile ID | 
**PhoneNumberId** | **string** | The selected phone number ID (from listWhatsAppPhoneNumbers) | 
**WabaId** | **string** | The WABA ID containing the selected phone | 
**TempToken** | **string** | The temporary access token from the headless redirect. Required unless sent in the X-Temp-Token header. | [optional] 
**ConnectFlow** | **string** | Set by the Zernio-hosted picker, whose user token stays in an httpOnly cookie. Integrators send tempToken instead. | [optional] 
**UserProfile** | **Object** | Optional user profile data (passthrough) | [optional] 
**RedirectUrl** | **string** | Optional URL to receive the post-connection redirect target | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

