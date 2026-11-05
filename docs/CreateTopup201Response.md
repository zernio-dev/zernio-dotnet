# Zernio.Model.CreateTopup201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TopupId** | **string** |  | 
**AmountCents** | **int** | Charged and credited to your balance once paid. | 
**FeeCents** | **int** | Always 0: there is no card fee. Kept for older clients. | 
**ChargedCents** | **int** | What the card is charged: amountCents. Kept for older clients. | 
**FeeIsExact** | **bool** | Always true. Kept for older clients. | 
**Status** | **string** |  | 
**ClientSecret** | **string** | PaymentIntent client secret for Stripe.js handleNextAction; set only when status is requires_action | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

