# Zernio.Model.GetWhatsAppCallingConfig200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumberDocId** | **string** | WhatsAppPhoneNumber Mongo ID (use on /v1/whatsapp/phone-numbers/{id}/calling) | [optional] 
**PhoneNumber** | **string** |  | [optional] 
**CallingEnabled** | **bool** |  | [optional] 
**ForwardTo** | **string** | tel:+E164 / sip:... / wss://... destination | [optional] 
**RecordingEnabled** | **bool** |  | [optional] 
**SipAuthUsername** | **string** |  | [optional] 
**SipAuthPasswordConfigured** | **bool** | True when a SIP digest password is stored. The plaintext is never returned. | [optional] 
**CallIconCountries** | **List&lt;string&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

