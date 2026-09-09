# Zernio.Model.ConnectWhatsAppEmbeddedSignupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **string** | Authorization code from the WA_EMBEDDED_SIGNUP postMessage | 
**ProfileId** | **string** |  | 
**WabaId** | **string** | WhatsApp Business Account id, when the SDK reported one | [optional] 
**PhoneNumberId** | **string** |  | [optional] 
**IsCoexistence** | **bool** | Number is also live in the WhatsApp Business app | [optional] 
**ExpectedPhoneNumber** | **string** | Rejects the connect when Meta returns a different number | [optional] 
**RedirectUrl** | **string** | Hosted signup page only. When present, the response also carries &#x60;redirectUrl&#x60;, the URL the user should land on, with the outcome mapped exactly like the redirect flow (success params, or &#x60;error&#x60; and &#x60;platform&#x60; with the same values). Must be an absolute http(s) URL or a custom app scheme. | [optional] 
**EchoConnectToken** | **bool** | Hosted signup page only. Append the connect token to the success redirect, as the redirect flow does for API-key callers. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

