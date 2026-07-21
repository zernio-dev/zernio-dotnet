# Zernio.Model.CheckPhoneNumberPortability200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PhoneNumber** | **string** |  | [optional] 
**Portable** | **bool** |  | [optional] 
**FastPortable** | **bool** | Qualifies for the carrier&#39;s accelerated FastPort lane. | [optional] 
**LineType** | **string** | Line type when known (mobile, landline, voip…). A US/CA mobile number requires the transfer PIN at submit. | [optional] 
**CountryCode** | **string** | ISO country of the number — pass it to GET /v1/phone-numbers/port-in/requirements for international numbers. | [optional] 
**PhoneNumberType** | **string** | Carrier number-type classification (local, mobile, national, toll_free…) — the numberType for the requirements endpoint. | [optional] 
**NotPortableReason** | **string** | Carrier reason when not portable; null when portable. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

