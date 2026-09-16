# Zernio.Model.ProductVariant
A purchasable variant of a product (one per option combination).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native variant id (numeric string for Shopify). | [optional] 
**Title** | **string** | Option combination label, e.g. \&quot;S / Blue\&quot;. | [optional] 
**Sku** | **string** |  | [optional] 
**Barcode** | **string** |  | [optional] 
**Price** | **string** | Decimal amount in the store currency, e.g. \&quot;19.90\&quot;. | [optional] 
**CompareAtPrice** | **string** | Strike-through price; null when the variant is not on sale. | [optional] 
**InventoryQuantity** | **int?** | Units on hand across locations; null when inventory is not tracked. | [optional] 
**AvailableForSale** | **bool** |  | [optional] 
**SelectedOptions** | [**List&lt;ProductVariantSelectedOptionsInner&gt;**](ProductVariantSelectedOptionsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

