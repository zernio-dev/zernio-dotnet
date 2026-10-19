# Zernio.Model.CommerceOrder
An order with what an invoice needs. Every amount is in `currency`, the store currency.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Number** | **string** | The number the merchant and buyer see. | [optional] 
**Status** | **CommerceOrderStatus** |  | [optional] 
**PlatformStatus** | **string** | Shopify fulfilment status (e.g. UNFULFILLED) or WooCommerce order status (e.g. processing). | [optional] 
**PaymentStatus** | **string** |  | [optional] 
**PlatformPaymentStatus** | **string** | Shopify financial status. Null on WooCommerce, where payment is read from the order status. | [optional] 
**Currency** | **string** |  | [optional] 
**TaxesIncluded** | **bool** | Whether line item and shipping amounts include tax. Always false on WooCommerce, whose API returns amounts before tax whatever the store displays (platformData.pricesIncludeTax). | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 
**PaidAt** | **DateTime?** | WooCommerce only; null on Shopify. | [optional] 
**CancelledAt** | **DateTime?** | Shopify only; null on WooCommerce. | [optional] 
**CancelReason** | **string** |  | [optional] 
**Subtotal** | [**CommerceMoney**](CommerceMoney.md) | Line items before order discounts and shipping. | [optional] 
**DiscountTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**ShippingTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**TaxTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Total** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**RefundedTotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**DiscountCodes** | **List&lt;string&gt;** |  | [optional] 
**PaymentMethods** | **List&lt;string&gt;** |  | [optional] 
**Customer** | [**CommerceOrderCustomer**](CommerceOrderCustomer.md) |  | [optional] 
**BillingAddress** | [**CommerceAddress**](CommerceAddress.md) |  | [optional] 
**ShippingAddress** | [**CommerceAddress**](CommerceAddress.md) |  | [optional] 
**BuyerNote** | **string** |  | [optional] 
**LineItems** | [**List&lt;CommerceOrderLineItemsInner&gt;**](CommerceOrderLineItemsInner.md) |  | [optional] 
**ShippingLines** | [**List&lt;CommerceOrderChargeLine&gt;**](CommerceOrderChargeLine.md) |  | [optional] 
**FeeLines** | [**List&lt;CommerceOrderChargeLine&gt;**](CommerceOrderChargeLine.md) | WooCommerce fees. Always empty on Shopify. | [optional] 
**TaxLines** | [**List&lt;CommerceTaxLine&gt;**](CommerceTaxLine.md) | Order tax by rate, line items and shipping together. | [optional] 
**Refunds** | [**List&lt;CommerceOrderRefundsInner&gt;**](CommerceOrderRefundsInner.md) |  | [optional] 
**Fulfillments** | [**List&lt;CommerceOrderFulfillmentsInner&gt;**](CommerceOrderFulfillmentsInner.md) |  | [optional] 
**PlatformData** | **Dictionary&lt;string, Object&gt;** | Platform-only fields. Null when the platform has none. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

