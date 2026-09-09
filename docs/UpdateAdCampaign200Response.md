# Zernio.Model.UpdateAdCampaign200Response
Echoes back only the fields you sent, plus `updated`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Updated** | **int** | Local Ad documents mirrored. 0 on the empty-campaign path. | [optional] 
**Budget** | [**AdCampaignBudget**](AdCampaignBudget.md) |  | [optional] 
**BudgetLevel** | **string** |  | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal** |  | [optional] 
**RoasAverageFloor** | **decimal** |  | [optional] 
**PortfolioBidStrategyId** | **string** | Google only. Echoed back, but NOT mirrored onto local Ad documents (no column for it yet). | [optional] 
**PlatformSpecificData** | **Object** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

