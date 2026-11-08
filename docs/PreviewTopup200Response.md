# Zernio.Model.PreviewTopup200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AmountCents** | **int** | Credited to your balance. | 
**TaxCents** | **int** | Tax added on top (VAT where it applies). | 
**TotalCents** | **int** | What the card would be charged: amountCents + taxCents. | 
**TaxLabel** | **string** | The tax and its rate, for example \&quot;VAT 21%\&quot;. Null when no tax is charged. | 
**ReverseCharge** | **bool** | True for an EU business with a valid VAT id: no VAT, reverse charge. | 
**Country** | **string** | Two-letter country the tax was placed in, from the billing address. Null when Stripe Tax returned no address. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

