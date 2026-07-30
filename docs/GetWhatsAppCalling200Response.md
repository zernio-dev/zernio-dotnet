# Zernio.Model.GetWhatsAppCalling200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumber** | **string** |  | [optional] 
**CallingEnabled** | **bool** |  | [optional] 
**CallDeepLink** | **string** | Public calling deep link (https://wa.me/call/&lt;number&gt;). Null while calling is disabled. | [optional] 
**ForwardTo** | **string** | tel:+E164 / sip:... / wss://... destination | [optional] 
**RecordingEnabled** | **bool** |  | [optional] 
**SipAuthUsername** | **string** |  | [optional] 
**SipAuthPasswordConfigured** | **bool** | True when a SIP digest password is stored. The plaintext is never returned. | [optional] 
**CallIconCountries** | **List&lt;string&gt;** |  | [optional] 
**OutboundDisabled** | **bool** | True when the number&#39;s country blocks business-initiated (outbound) WhatsApp calling; inbound still works. | [optional] 
**CallerIdMode** | **string** | Caller ID the forward-leg callee sees on tel: forwards. business &#x3D; this WhatsApp number; platform &#x3D; a Zernio number (used when the number was brought by the customer and its caller ID is not verified for PSTN origination). | [optional] 
**CallerIdVerified** | **bool** | True once the number completed caller-ID verification, making tel: forwards display the business number itself. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

