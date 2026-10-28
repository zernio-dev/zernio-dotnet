# Zernio.Model.WebhookPayloadCampaignPayoutPayoutFailure
Present on campaign_payout.failed only.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TransferId** | **string** | The Zernio transfer that did not go through. | 
**AmountCents** | **int** | The payout amount that did not reach the creator. It is returned to payable, minus any amount a rejection made while the payout was in flight claws back to the campaign budget; payableCents is the balance after both. | 
**Reason** | **string** | returned: Stripe refused the transfer. stale: it could not be confirmed with Stripe within 24 hours. reversed: Stripe reversed it after it was sent; the settlement is undone. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

