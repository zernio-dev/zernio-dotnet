# Zernio.Model.GetBalance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvailableCents** | **int** | Your balance. It goes negative after a dispute or refund of funds already spent, or when pay-per-use already in flight lands past zero. The next funds you add cover it. New payout batches are refused while it is negative. | [optional] 
**BalanceBilling** | **bool** | True when the account pays pay-per-use from this prepaid balance (new signups). Absent otherwise: that pay-per-use is on the monthly invoice. | [optional] 
**SpendableCents** | **int** | Balance billing only (absent otherwise). What pay-per-use can still spend: availableCents plus promoCents, minus usage not yet posted. At 0 or below, new pay-per-use answers 402 &#x60;insufficient_balance&#x60;. | [optional] 
**PromoCents** | **int** | Balance billing only (absent otherwise). Promotional and support credit Zernio added to your balance. Pay-per-use spends it before availableCents. It is never paid out to payees and is not part of availableCents. | [optional] 
**PayoutLockedCents** | **int** | Always 0. The balance no longer pays creators, so none of it is locked from them. | [optional] 
**PayoutLocks** | [**List&lt;GetBalance200ResponsePayoutLocksInner&gt;**](GetBalance200ResponsePayoutLocksInner.md) | Always empty. The balance no longer pays creators. | [optional] 
**PendingCents** | **int** | Card top-ups paid before 2026-10-29 that were held and are moving to availableCents (within the hour). Always 0 after that. | [optional] 
**PendingReleases** | [**List&lt;GetBalance200ResponsePendingReleasesInner&gt;**](GetBalance200ResponsePendingReleasesInner.md) | The held card top-ups behind pendingCents. | [optional] 
**PendingTopupCents** | **int** | Top-ups started but not paid yet. | [optional] 
**Currency** | **string** |  | [optional] 
**RecentTopups** | [**List&lt;TreasuryTopup&gt;**](TreasuryTopup.md) |  | [optional] 
**RecentCreditRecharges** | [**List&lt;GetBalance200ResponseRecentCreditRechargesInner&gt;**](GetBalance200ResponseRecentCreditRechargesInner.md) | Balance billing only (absent otherwise). The 10 newest auto top-ups paid from the account credit you held when you moved to the balance, newest first. Nothing was charged to your card and there is no invoice. The amount was added to promoCents with the credit&#39;s own expiry. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

