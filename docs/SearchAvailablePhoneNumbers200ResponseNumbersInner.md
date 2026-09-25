# Zernio.Model.SearchAvailablePhoneNumbers200ResponseNumbersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumber** | **string** | E.164. Pass it as &#x60;phoneNumber&#x60; on POST /v1/phone-numbers/purchase to buy this exact number. | [optional] 
**Features** | **List&lt;string&gt;** | Provider capability list for this number (e.g. voice, sms, mms). | [optional] 
**Locality** | **string** | Town or rate center the number belongs to, as the carrier names it (e.g. WACO). | [optional] 
**BestEffort** | **bool** | true when the carrier added this number because too few matched your filters, so it may be outside the requested prefix or locality. | [optional] 
**MaskedNumber** | **string** | Keyless calls only, in place of &#x60;phoneNumber&#x60;: the number with its middle digits masked, e.g. +44 20 •••• 0123. | [optional] 
**NumberType** | **string** | Keyless calls only. Without a &#x60;numberType&#x60; filter a keyless search mixes every type the country sells, so each result names its own. | [optional] 
**ClaimId** | **string** | Keyless calls only. Opaque, expires after 7 days. Pass it as &#x60;claimId&#x60; on a keyless POST /v1/phone-numbers/purchase. | [optional] 
**ClaimUrl** | **string** | Keyless calls only. Signup link that opens the dashboard&#39;s confirm step for this number. The number is not held: if it is gone by then, the buyer picks another in the same area. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

