# Zernio.Model.SubmitPhoneNumberKyc200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** |  | [optional] 
**PreOrder** | **bool** | True when nothing was in stock and this submission placed a pre-order. The number stays &#x60;pending_regulatory&#x60; until the carrier sources it (usually about 3 weeks) and is not billed until active. A pre-order is one number: &#x60;quantity&#x60; above 1 is rejected with 400. | [optional] 
**PhoneNumber** | [**SubmitPhoneNumberKyc200ResponsePhoneNumber**](SubmitPhoneNumberKyc200ResponsePhoneNumber.md) |  | [optional] 
**Numbers** | [**List&lt;SubmitPhoneNumberKyc200ResponseNumbersInner&gt;**](SubmitPhoneNumberKyc200ResponseNumbersInner.md) | Every number provisioned from this submission. Length equals the requested &#x60;quantity&#x60; on full success (fewer if some orders failed; best-effort). The first element mirrors &#x60;phoneNumber&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

