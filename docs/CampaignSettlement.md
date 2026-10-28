# Zernio.Model.CampaignSettlement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EntryId** | **string** | The ledger settlement entry. | 
**ParticipantId** | **string** |  | 
**AmountCents** | **int** |  | 
**ExternalReference** | **string** |  | 
**PayableCents** | **int** | Payable balance left after this settlement. | 
**SettledAt** | **DateTime** |  | 
**TransferId** | **string** | Treasury settlement only: the Zernio transfer that moved the money. The creator receives amountCents in full. | [optional] 
**FeeCents** | **int** | Treasury settlement only: the transfer fee, added on top of amountCents. | [optional] 
**TotalCents** | **int** | Treasury settlement only: debited from your balance, amountCents plus feeCents. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

