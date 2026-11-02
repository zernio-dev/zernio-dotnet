# Zernio.Model.CreateTopup201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TopupId** | **string** |  | 
**AmountCents** | **int** | Credited to your balance once paid: exactly this when feeIsExact, else at least this. | 
**FeeCents** | **int** | Card fee, charged on top of amountCents. | 
**ChargedCents** | **int** | What the card is charged: amountCents plus feeCents. | 
**FeeIsExact** | **bool** | True when feeCents is exactly Stripe&#39;s fee for this card. False when it is the region&#39;s highest rate, so Stripe may take less and the difference is added to your balance. | 
**Status** | **string** |  | 
**ClientSecret** | **string** | PaymentIntent client secret for Stripe.js handleNextAction; set only when status is requires_action | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

