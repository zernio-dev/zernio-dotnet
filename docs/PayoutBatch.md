# Zernio.Model.PayoutBatch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**CampaignId** | **string** |  | 
**Status** | **string** | &#x60;awaiting_payment&#x60; until the card charge succeeds (3D Secure included); &#x60;paying&#x60; while transfers go out; then &#x60;paid&#x60;, &#x60;partially_failed&#x60; (some items failed or were skipped), &#x60;failed&#x60; (the card was declined, or none paid) or &#x60;expired&#x60; (the payment was cancelled unpaid, every amount is payable again). | 
**Method** | **string** |  | 
**AmountCents** | **int** | Total the creators receive. | 
**FeeCents** | **int** | Total Zernio fee. | 
**TotalCents** | **int** | The card charge: amountCents plus feeCents. | 
**Items** | [**List&lt;PayoutBatchItem&gt;**](PayoutBatchItem.md) |  | 
**PaidAt** | **DateTime?** |  | 
**FinishedAt** | **DateTime?** |  | 
**CreatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

