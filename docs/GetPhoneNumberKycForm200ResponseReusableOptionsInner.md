# Zernio.Model.GetPhoneNumberKycForm200ResponseReusableOptionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Opaque option id — pass as &#x60;reuseOptionId&#x60; on POST. Stable selection key (a phone number is not unique across verifications). | [optional] 
**FromPhoneNumber** | **string** | Display only — the number this verification was submitted for. Not a selection key. | [optional] 
**Instant** | **bool** | true &#x3D; group-approved, a new order activates in minutes; false &#x3D; documents are reused but the order still queues for carrier review (1-3 days). | [optional] 
**Details** | [**List&lt;GetPhoneNumberKycForm200ResponseReusableOptionsInnerDetailsInner&gt;**](GetPhoneNumberKycForm200ResponseReusableOptionsInnerDetailsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

