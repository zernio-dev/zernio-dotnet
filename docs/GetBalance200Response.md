# Zernio.Model.GetBalance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvailableCents** | **int** | Your balance. It goes negative after a dispute or refund of a spent top-up, or when pay-per-use already in flight lands past zero. The next top-up covers it. New payout batches are refused while it is negative. | [optional] 
**PromoCents** | **int** | Balance billing only (absent otherwise). Promotional and support credit Zernio added to your balance. Pay-per-use spends it before availableCents. It is never paid out to payees and is not part of availableCents. | [optional] 
**PayoutLockedCents** | **int** | Always 0. The balance no longer pays creators, so none of it is locked from them. | [optional] 
**PayoutLocks** | [**List&lt;GetBalance200ResponsePayoutLocksInner&gt;**](GetBalance200ResponsePayoutLocksInner.md) | Always empty. The balance no longer pays creators. | [optional] 
**PendingCents** | **int** | Card top-ups paid before 2026-10-29 that were held and are moving to availableCents (within the hour). Always 0 after that. | [optional] 
**PendingReleases** | [**List&lt;GetBalance200ResponsePendingReleasesInner&gt;**](GetBalance200ResponsePendingReleasesInner.md) | The held card top-ups behind pendingCents. | [optional] 
**PendingTopupCents** | **int** | Top-ups started but not paid yet. | [optional] 
**Currency** | **string** |  | [optional] 
**RecentTopups** | [**List&lt;TreasuryTopup&gt;**](TreasuryTopup.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

