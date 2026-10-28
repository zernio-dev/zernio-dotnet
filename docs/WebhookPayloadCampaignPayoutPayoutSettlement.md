# Zernio.Model.WebhookPayloadCampaignPayoutPayoutSettlement
Present on campaign_payout.settled only.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EntryId** | **string** | The ledger settlement entry. | 
**AmountCents** | **int** |  | 
**ExternalReference** | **string** |  | 
**Recorded** | **bool** | True when the payout was made outside Zernio and only recorded here; false when Zernio moved the money through the treasury. | 
**TransferId** | **string** | Treasury settlement only: the Zernio transfer that moved the money. The creator receives amountCents in full. | [optional] 
**FeeCents** | **int** | Treasury settlement only: the transfer fee, added on top of amountCents. | [optional] 
**TotalCents** | **int** | Treasury settlement only: debited from your balance, amountCents plus feeCents. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

