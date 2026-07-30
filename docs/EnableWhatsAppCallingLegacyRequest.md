# Zernio.Model.EnableWhatsAppCallingLegacyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**ForwardTo** | **string** | tel:+E164 / sip:... / wss://... destination | 
**SipAuthUsername** | **string** |  | [optional] 
**SipAuthPassword** | **string** | Stored encrypted, never returned by any endpoint. | [optional] 
**RecordingEnabled** | **bool** |  | [optional] [default to false]
**CallIconCountries** | **List&lt;string&gt;** |  | [optional] 
**MaxCallDurationSeconds** | **int** | Hard cap (seconds) on a forwarded call; the carrier hangs up both legs when it fires. Safety valve against dead-air billing when a destination hangs up but the signal is lost. | [optional] 
**ForwardCallerId** | **string** | Caller ID presented to the forward destination. caller &#x3D; the WhatsApp user&#39;s number (sip: destinations only; ignored on tel: forwards). Fixes AI-agent trunks that reject seeing the business number call itself. | [optional] [default to ForwardCallerIdEnum.Business]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

