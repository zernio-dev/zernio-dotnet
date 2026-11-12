# Zernio.Model.CreateCommerceDraftOrderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Connected store SocialAccount id. | 
**CustomerId** | **string** | The customer it is for, from the customers endpoints. | [optional] 
**Email** | **string** |  | [optional] 
**LineItems** | [**List&lt;CreateCommerceDraftOrderRequestLineItemsInner&gt;**](CreateCommerceDraftOrderRequestLineItemsInner.md) | A product variant (variantId) or a custom item (title and price). | 
**Discount** | [**CreateCommerceDraftOrderRequestDiscount**](CreateCommerceDraftOrderRequestDiscount.md) |  | [optional] 
**Shipping** | [**CreateCommerceDraftOrderRequestShipping**](CreateCommerceDraftOrderRequestShipping.md) |  | [optional] 
**ShippingAddress** | [**CreateCommerceDraftOrderRequestShippingAddress**](CreateCommerceDraftOrderRequestShippingAddress.md) |  | [optional] 
**Note** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

