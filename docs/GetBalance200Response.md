# Zernio.Model.GetBalance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvailableCents** | **int** | Your balance, including card top-ups paid in the last 7 days (see payoutLockedCents). Negative after a dispute or refund of a top-up that was already spent; transfers are refused while it is negative. | [optional] 
**PayoutLockedCents** | **int** | Part of availableCents from card top-ups charged in the last 7 days, net of refunds and disputes. Transfers to payees cannot use it yet; a transfer that needs it answers 409 &#x60;payout_funds_locked&#x60; with the day it can be sent. | [optional] 
**PayoutLocks** | [**List&lt;GetBalance200ResponsePayoutLocksInner&gt;**](GetBalance200ResponsePayoutLocksInner.md) | The card top-ups behind payoutLockedCents, soonest first. | [optional] 
**PendingCents** | **int** | Card top-ups paid before 2026-10-29 that were held and are moving to availableCents (within the hour). Always 0 after that. | [optional] 
**PendingReleases** | [**List&lt;GetBalance200ResponsePendingReleasesInner&gt;**](GetBalance200ResponsePendingReleasesInner.md) | The held card top-ups behind pendingCents. | [optional] 
**PendingTopupCents** | **int** | Top-ups started but not paid yet. | [optional] 
**Currency** | **string** |  | [optional] 
**RecentTopups** | [**List&lt;TreasuryTopup&gt;**](TreasuryTopup.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

