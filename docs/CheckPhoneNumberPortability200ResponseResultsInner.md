# Zernio.Model.CheckPhoneNumberPortability200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumber** | **string** |  | [optional] 
**Portable** | **bool** |  | [optional] 
**FastPortable** | **bool** | Qualifies for the carrier&#39;s accelerated FastPort lane. | [optional] 
**MessagingCapable** | **bool?** | Whether texting can be enabled on the number once ported; null when the carrier does not say. | [optional] 
**LineType** | **string** | Line type when known (mobile, landline, voip, toll-free, unknown). US/CA portable numbers only. A US/CA mobile number requires the transfer PIN at submit. | [optional] 
**CarrierName** | **string** | The number&#39;s current carrier, when the lookup knows it. US/CA portable numbers only. | [optional] 
**CountryCode** | **string** | ISO country of the number. Pass it to GET /v1/phone-numbers/port-in/requirements for international numbers. | [optional] 
**PhoneNumberType** | **string** | Carrier number-type classification (local, mobile, national, toll_free...), the numberType for the requirements endpoint. | [optional] 
**NotPortableReason** | **string** | Carrier reason when not portable; null when portable. | [optional] 
**ClaimId** | **string** | Keyless calls and claimLinks&#x3D;true only, on portable results. Resolve it with GET /v1/phone-numbers/port-in/claims/{claimId}. Expires after 7 days. | [optional] 
**ClaimUrl** | **string** | Keyless calls and claimLinks&#x3D;true only, on portable results. A signup link that lands on the dashboard&#39;s port form with this number filled in. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

