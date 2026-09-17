# Zernio.Model.BoostPostRequestPromoCodesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DiscountType** | **string** |  | 
**DiscountValue** | **decimal** | PERCENTAGE: integer 1-100. CASH: amount greater than 0 in discountCurrency. | 
**DiscountCurrency** | **string** | ISO 4217; required for CASH. | [optional] 
**PromoCode** | **string** | Code entered at checkout; omit for an automatic offer. | [optional] 
**MinimumPurchaseType** | **string** |  | [optional] 
**MinimumPurchaseValue** | **decimal** | Required with minimumPurchaseType; QUANTITY is an integer &gt;&#x3D; 0, SUBTOTAL an amount &gt; 0. | [optional] 
**MinimumPurchaseCurrency** | **string** | ISO 4217; required for SUBTOTAL. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

