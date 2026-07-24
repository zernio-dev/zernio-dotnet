# Zernio.Model.CheckPhoneNumberAvailability200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Country** | **string** |  | [optional] 
**NumberType** | **string** |  | [optional] 
**Available** | **bool** | Whether deliverable voice inventory exists right now. | [optional] 
**AddressConstraint** | **string** |  | [optional] 
**Areas** | **List&lt;string&gt;** | For &#x60;geo&#x60; only — the area(s) the registered address must be in. | [optional] 
**AreaOptions** | [**List&lt;CheckPhoneNumberAvailability200ResponseAreaOptionsInner&gt;**](CheckPhoneNumberAvailability200ResponseAreaOptionsInner.md) | Live inventory grouped by area code, largest stock first. Empty when out of stock (or the area lookup failed). Pass a chosen &#x60;ndc&#x60; as &#x60;areaCode&#x60; on POST /v1/phone-numbers/purchase (or on the KYC submit for regulated countries) to require that area.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

