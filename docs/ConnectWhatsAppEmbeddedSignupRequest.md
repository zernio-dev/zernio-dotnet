# Zernio.Model.ConnectWhatsAppEmbeddedSignupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **string** | Authorization code from the FB.login response (authResponse.code) | 
**ProfileId** | **string** |  | 
**WabaId** | **string** | waba_id from the WA_EMBEDDED_SIGNUP message event | [optional] 
**PhoneNumberId** | **string** | phone_number_id from the WA_EMBEDDED_SIGNUP message event. With wabaId it skips the number picker. | [optional] 
**IsCoexistence** | **bool** | Set when the popup ended with the FINISH_WHATSAPP_BUSINESS_APP_ONBOARDING event, so the number stays live in the WhatsApp Business app | [optional] 
**ExpectedPhoneNumber** | **string** | Rejects the connect when Meta returns a different number | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

