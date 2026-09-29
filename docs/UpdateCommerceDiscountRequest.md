# Zernio.Model.UpdateCommerceDiscountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**Title** | **string** |  | [optional] 
**Code** | **string** | Required for method code. | [optional] 
**Percentage** | **decimal** | For type percentage, e.g. 15 for 15%. | [optional] 
**Amount** | **string** | For type fixed_amount, a decimal in the store currency. | [optional] 
**AppliesOnEachItem** | **bool** | fixed_amount only: take the amount off each item instead of once per order. | [optional] 
**MinimumSubtotal** | **string** | Minimum order subtotal, a decimal in the store currency. | [optional] 
**MinimumQuantity** | **int?** |  | [optional] 
**UsageLimit** | **int?** | Code discounts only: total uses allowed. | [optional] 
**OncePerCustomer** | **bool** | Code discounts only. | [optional] 
**StartsAt** | **DateTime** | Defaults to now. | [optional] 
**EndsAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

