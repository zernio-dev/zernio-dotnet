# Zernio.Model.CreatorCampaignEconomicsAdPerformance
Pays on what the ads running a post achieve. `spend` and `purchase_value` take `rateBps` (a share of the amount), `purchases` and `clicks` take `centsPerUnit` each, and `impressions` takes `centsPerUnit` per 1,000.  Sending the other rate field, or `organicViewsOnly`, answers 400. Every campaign platform must be Instagram, Facebook or TikTok. Money from an ad billed in another currency than the campaign does not count. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Metric** | **string** |  | 
**RateBps** | **int** | Basis points of the spend or purchase value: 1000 is 10%. | [optional] 
**CentsPerUnit** | **int** | Cents per purchase or click, or per 1,000 impressions. | [optional] 
**MaxPayoutPerPostCents** | **int** |  | [optional] 
**BudgetCents** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

