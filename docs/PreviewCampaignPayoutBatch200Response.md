# Zernio.Model.PreviewCampaignPayoutBatch200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PayoutCount** | **int** | Creators who would be paid. | 
**AmountCents** | **int** | Total the creators receive. | 
**FeeCents** | **int** | Zernio fee: 4% per creator, 50 cent minimum. | 
**TaxCents** | **int** | VAT on the fee, 0 when none applies. | 
**TotalCents** | **int** | What the card would be charged: amountCents + feeCents + taxCents. | 
**TaxLabel** | **string** | For example \&quot;VAT 21%\&quot;. Null when there is no tax. | 
**ReverseCharge** | **bool** | The fee is reverse charged: you account for the VAT. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

