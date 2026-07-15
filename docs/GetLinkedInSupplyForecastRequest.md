# Zernio.Model.GetLinkedInSupplyForecastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**AdAccountId** | **string** |  | 
**Spec** | [**TargetingSpec**](TargetingSpec.md) |  | 
**CampaignType** | **string** | Defaults to SPONSORED_UPDATES. | [optional] 
**TimeRangeStart** | **int** | Unix ms. Must be in the future. | 
**TimeRangeEnd** | **int** | Unix ms. Must be after start and within LinkedIn&#39;s max horizon. | 
**ObjectiveType** | **string** |  | [optional] 
**OptimizationTarget** | **string** | When set, the forecast assumes auto-bidding. When unset, competingBid is required. | [optional] 
**DailyBudget** | **decimal** | Either dailyBudget or totalBudget is required. | [optional] 
**TotalBudget** | **decimal** |  | [optional] 
**Currency** | **string** | ISO 4217, defaults to USD. | [optional] 
**CompetingBid** | [**GetLinkedInSupplyForecastRequestCompetingBid**](GetLinkedInSupplyForecastRequestCompetingBid.md) |  | [optional] 
**EnableAudienceNetwork** | **bool** | Defaults to false. Required true for connectedTelevisionOnly. | [optional] 
**EnableAudienceExpansion** | **bool** | Defaults to false. | [optional] 
**ConnectedTelevisionOnly** | **bool** | Defaults to false. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

