# Zernio.Model.CreateTopup201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TopupId** | **string** |  | 
**AmountCents** | **int** | Credited to your balance once paid. | 
**TaxCents** | **int** | Tax added on top of amountCents (VAT where it applies). 0 when reverse charged or outside the EU. | 
**TotalCents** | **int** | What the card is charged: amountCents + taxCents. | 
**TaxLabel** | **string** | The tax and its rate, for example \&quot;VAT 21%\&quot;. Null when no tax is charged. | 
**ReverseCharge** | **bool** | True for an EU business with a valid VAT id: no VAT is charged and the invoice says reverse charge. | 
**FeeCents** | **int** | Always 0: there is no card fee. Kept for older clients. | 
**ChargedCents** | **int** | Same as totalCents. Kept for older clients. | 
**FeeIsExact** | **bool** | Always true. Kept for older clients. | 
**Status** | **string** |  | 
**ClientSecret** | **string** | PaymentIntent client secret for Stripe.js handleNextAction; set only when status is requires_action | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

