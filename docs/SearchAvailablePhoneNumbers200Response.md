# Zernio.Model.SearchAvailablePhoneNumbers200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Country** | **string** |  | [optional] 
**NumberType** | **string** |  | [optional] 
**RequireSms** | **bool** | Echo of the &#x60;sms&#x60; filter applied to this search. | [optional] 
**Numbers** | [**List&lt;SearchAvailablePhoneNumbers200ResponseNumbersInner&gt;**](SearchAvailablePhoneNumbers200ResponseNumbersInner.md) |  | [optional] 
**Masked** | **bool** | true on keyless calls. | [optional] 
**Near** | **string** | With &#x60;country&#x3D;auto&#x60;: the caller&#39;s city the results were narrowed to, or null when there was no stock there. | [optional] 
**ClaimId** | **string** | Keyless calls only: a claim for any number matching this search&#39;s country, type and area. | [optional] 
**ClaimUrl** | **string** | Keyless calls only: signup link for any number matching this search. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

