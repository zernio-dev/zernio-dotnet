# Zernio.Model.CommerceVariant
A purchasable variant of a product (one per option combination).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native variant id. | [optional] 
**Title** | **string** | Option combination label, e.g. \&quot;S / Blue\&quot;. | [optional] 
**Sku** | **string** |  | [optional] 
**Barcode** | **string** |  | [optional] 
**Price** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**CompareAtPrice** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**InventoryQuantity** | **int?** | Units on hand; null when inventory is not tracked. | [optional] 
**AvailableForSale** | **bool?** |  | [optional] 
**Options** | [**List&lt;CreateCommerceProductVariantsRequestVariantsInnerOptionsInner&gt;**](CreateCommerceProductVariantsRequestVariantsInnerOptionsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

