# Zernio.Model.GoogleRecommendation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ResourceName** | **string** | customers/{customerId}/recommendations/{id}. Pass it to apply or dismiss. | 
**Id** | **string** |  | 
**Type** | **string** | Google RecommendationType, such as CAMPAIGN_BUDGET, KEYWORD or SET_TARGET_CPA. | 
**Dismissed** | **bool** |  | 
**CampaignId** | **string** |  | 
**CampaignIds** | **List&lt;string&gt;** | Every campaign the recommendation targets (several for account-level types). | 
**AdGroupId** | **string** |  | 
**CampaignBudgetId** | **string** |  | 
**Impact** | [**GoogleRecommendationImpact**](GoogleRecommendationImpact.md) |  | 
**Details** | **Object** | The type-specific recommendation payload exactly as Google returns it (camelCase, amounts in micros), for example recommendedTargetCpaMicros or budgetOptions. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

