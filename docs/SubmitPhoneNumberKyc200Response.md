# Zernio.Model.SubmitPhoneNumberKyc200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** |  | [optional] 
**PhoneNumber** | [**SubmitPhoneNumberKyc200ResponsePhoneNumber**](SubmitPhoneNumberKyc200ResponsePhoneNumber.md) |  | [optional] 
**Numbers** | [**List&lt;SubmitPhoneNumberKyc200ResponseNumbersInner&gt;**](SubmitPhoneNumberKyc200ResponseNumbersInner.md) | Every number provisioned from this submission. Length equals the requested &#x60;quantity&#x60; on full success (fewer if some orders failed; best-effort). The first element mirrors &#x60;phoneNumber&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

