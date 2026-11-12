# Zernio.Model.CommerceRefundPreview
What a refund would return, computed by the platform. Amounts are in the currency the buyer paid in, which refunds are made in.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**MaximumRefundable** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Subtotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Tax** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Shipping** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**LineItems** | [**List&lt;CommerceRefundPreviewLineItemsInner&gt;**](CommerceRefundPreviewLineItemsInner.md) |  | [optional] 
**Transactions** | [**List&lt;CommerceRefundPreviewTransactionsInner&gt;**](CommerceRefundPreviewTransactionsInner.md) | The payments the money goes back to. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

