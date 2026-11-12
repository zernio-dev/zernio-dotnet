# Zernio.Model.CommerceDraftOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**InvoiceUrl** | **string** | The checkout link the buyer pays through. | [optional] 
**InvoiceSentAt** | **DateTime?** |  | [optional] 
**Email** | **string** |  | [optional] 
**CustomerId** | **string** |  | [optional] 
**Note** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**Currency** | **string** | The currency the buyer pays in; every amount uses it. | [optional] 
**Subtotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**DiscountTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**ShippingTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**TaxTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Total** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**LineItems** | [**List&lt;CommerceDraftOrderLineItemsInner&gt;**](CommerceDraftOrderLineItemsInner.md) |  | [optional] 
**ShippingAddress** | [**CommerceAddress**](CommerceAddress.md) |  | [optional] 
**OrderId** | **string** | The order it became once completed. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 
**CompletedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

