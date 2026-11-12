# Zernio.Model.CommerceOrderEditPreview
The order as the edit leaves it. Amounts are in the currency the buyer paid in.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subtotal** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Total** | [**CommerceMoney**](CommerceMoney.md) |  | [optional] 
**Outstanding** | [**CommerceMoney**](CommerceMoney.md) | What the buyer still owes. Negative when the edit leaves them overpaid: refund that with the refunds endpoint. | [optional] 
**LineItems** | [**List&lt;CommerceOrderEditPreviewLineItemsInner&gt;**](CommerceOrderEditPreviewLineItemsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

