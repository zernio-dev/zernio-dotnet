# Zernio.Model.PayoutBatchItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**ParticipantId** | **string** |  | 
**Creator** | [**PayoutBatchItemCreator**](PayoutBatchItemCreator.md) |  | 
**AmountCents** | **int** | What the creator receives, in full. | 
**FeeCents** | **int** | Zernio fee on top: 4%, 50 cents minimum per payout. | 
**TotalCents** | **int** | amountCents plus feeCents. | 
**Status** | **string** | &#x60;skipped&#x60;: payout setup not finished, or the card payment never completed. &#x60;failed&#x60;: Stripe refused the transfer. &#x60;refunded&#x60;: failed or skipped after the card hold; its payout, fee and VAT on the fee went back to the card through a credit note. The amount is payable again in every case. | 
**FailureReason** | **string** | Why the item was not paid, in plain words. | 
**TransferId** | **string** | The treasury transfer that paid this item. | 
**RefundedCents** | **int?** | What went back to the card for a &#x60;refunded&#x60; item: payout, fee and VAT on the fee. Null otherwise. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

