# Zernio.Model.GetLinkedInBidPricingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio social account ID (LinkedIn). | 
**AdAccountId** | **string** | LinkedIn ad account ID (numeric). | 
**Spec** | [**TargetingSpec**](TargetingSpec.md) | Same targeting spec used by POST /v1/ads/create. | 
**CampaignType** | **string** | Defaults to SPONSORED_UPDATES. | [optional] 
**BidType** | **string** | Defaults to CPM. | [optional] 
**MatchType** | **string** | Defaults to EXACT. | [optional] 
**Currency** | **string** | ISO 4217, defaults to USD. | [optional] 
**ObjectiveType** | **string** | LinkedIn objectiveType, e.g. WEBSITE_VISIT, LEAD_GENERATION, VIDEO_VIEW. | [optional] 
**OptimizationTargetType** | **string** | LinkedIn optimizationTargetType, e.g. MAX_CLICK, MAX_IMPRESSION. | [optional] 
**DailyBudget** | **decimal** | Optional daily budget in whole account-currency units. LinkedIn refines the suggested bid to this budget. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

