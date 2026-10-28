# Zernio.Model.PayoutBatchItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**ParticipantId** | **string** |  | 
**Creator** | [**PayoutBatchItemCreator**](PayoutBatchItemCreator.md) |  | 
**AmountCents** | **int** | What the creator receives, in full. | 
**FeeCents** | **int** | Zernio fee on top: 4% with a 50 cent minimum. | 
**TotalCents** | **int** | amountCents plus feeCents. | 
**Status** | **string** | &#x60;skipped&#x60;: not paid because payout setup was not finished, or the card payment never completed; the amount is payable again. &#x60;failed&#x60;: Stripe refused the transfer; the amount is payable again. | 
**FailureReason** | **string** | Why the item was not paid, in plain words. | 
**TransferId** | **string** | The treasury transfer that paid this item. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

