# Zernio.Model.TreasuryTopup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Method** | **string** |  | [optional] 
**Purpose** | **string** | &#x60;balance&#x60; funds your balance; &#x60;payout_batch&#x60; is the card payment of one payout batch, which pays its creators directly. | [optional] 
**PayoutBatch** | [**TreasuryTopupPayoutBatch**](TreasuryTopupPayoutBatch.md) |  | [optional] 
**FeeCoveredByZernio** | **bool** | True for a &#x60;payout_batch&#x60; payment: Zernio pays the Stripe processing fee out of its transfer fee, so you are credited the whole charge. | [optional] 
**AmountCents** | **int** | Gross amount charged | [optional] 
**StripeFeeCents** | **int?** | Stripe processing fee you paid; null until Stripe reports it, 0 when Zernio covers it | [optional] 
**NetCents** | **int?** | Amount credited to your balance: gross minus the Stripe fee, or the whole charge when Zernio covers the fee; null until Stripe reports it | [optional] 
**Status** | **string** | &#x60;pending&#x60; until the card is charged (or 3D Secure is finished) and credited. &#x60;expired&#x60; means it ended unpaid: cancelled, or 3D Secure left unfinished for 30 minutes. Only &#x60;pending&#x60; counts toward pendingTopupCents. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**SucceededAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

