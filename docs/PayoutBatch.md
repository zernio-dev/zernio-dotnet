# Zernio.Model.PayoutBatch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**CampaignId** | **string** |  | 
**Status** | **string** | &#x60;awaiting_payment&#x60; until the card charge succeeds (3D Secure included); &#x60;paying&#x60; during the 7-day card hold and while transfers go out; then &#x60;paid&#x60;, &#x60;partially_failed&#x60; (some items failed or were skipped), &#x60;failed&#x60; (the card was declined, or none paid) or &#x60;expired&#x60; (the payment was cancelled unpaid, every amount is payable again). | 
**Method** | **string** |  | 
**AmountCents** | **int** | Total the creators receive. | 
**FeeCents** | **int** | Total Zernio fee. | 
**TotalCents** | **int** | amountCents plus feeCents. The card is charged this plus the VAT on the fee where it applies (see the batch invoice). | 
**Items** | [**List&lt;PayoutBatchItem&gt;**](PayoutBatchItem.md) |  | 
**PaidAt** | **DateTime?** |  | 
**ReleasesAt** | **DateTime?** | When the 7-day card hold ends and the creators are paid. Null until the charge succeeds. | 
**FinishedAt** | **DateTime?** |  | 
**CreatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

