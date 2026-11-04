# Zernio.Model.GetTopupReceipt200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Url** | **string** |  | 
**Format** | **string** |  | 
**InvoiceUrl** | **string** | The invoice PDF; null when the payment made no invoice. | [optional] 
**ReceiptUrl** | **string** | Stripe&#39;s card receipt page for the charge. | [optional] 
**AmountCents** | **int** | As in the top-up list. | 
**FeeCents** | **int?** | Card fee paid, as in the top-up list. | 
**ChargedCents** | **int** | What the card was charged, the total on the receipt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

