# Zernio.Model.CommerceOrderLineItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**ProductId** | **string** | Null when the product was deleted. | [optional] 
**VariantId** | **string** |  | [optional] 
**Sku** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**VariantTitle** | **string** |  | [optional] 
**Quantity** | **int** | As ordered; refunded units are listed under refunds. | [optional] 
**UnitPrice** | [**CommerceMoney**](CommerceMoney.md) | Before discounts. | [optional] 
**Subtotal** | [**CommerceMoney**](CommerceMoney.md) | unitPrice x quantity. | [optional] 
**DiscountTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Total** | [**CommerceMoney**](CommerceMoney.md) | subtotal minus discountTotal. | [optional] 
**TaxLines** | [**List&lt;CommerceTaxLine&gt;**](CommerceTaxLine.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

