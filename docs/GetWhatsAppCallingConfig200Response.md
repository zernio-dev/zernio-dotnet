# Zernio.Model.GetWhatsAppCallingConfig200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumberDocId** | **string** | Phone number record ID (use on /v1/phone-numbers/{id}/whatsapp/calling) | [optional] 
**PhoneNumber** | **string** |  | [optional] 
**CallingEnabled** | **bool** |  | [optional] 
**CallDeepLink** | **string** | Public calling deep link (https://wa.me/call/&lt;number&gt;). Tapping it on a phone starts a WhatsApp voice call to this number. Embed it on websites, emails, or QR codes. Null while calling is disabled; not supported by WhatsApp desktop clients. | [optional] 
**ForwardTo** | **string** | tel:+E164 / sip:... / wss://... destination | [optional] 
**RecordingEnabled** | **bool** |  | [optional] 
**SipAuthUsername** | **string** |  | [optional] 
**SipAuthPasswordConfigured** | **bool** | True when a SIP digest password is stored. The plaintext is never returned. | [optional] 
**CallIconCountries** | **List&lt;string&gt;** |  | [optional] 
**CallerIdMode** | **string** | Caller ID the forward-leg callee sees on tel: forwards. business &#x3D; this WhatsApp number; platform &#x3D; a Zernio number (customer-brought number without verified caller ID; verify via /v1/phone-numbers/{id}/whatsapp/caller-id-verification). | [optional] 
**CallerIdVerified** | **bool** | True once the number completed caller-ID verification. | [optional] 
**MaxCallDurationSeconds** | **int?** | Hard cap (seconds) on forwarded calls; null &#x3D; no cap. | [optional] 
**ForwardCallerId** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

