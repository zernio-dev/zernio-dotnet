# Zernio.Model.CreateAdRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**AccountId** | **string** | The ads connection (account ID from &#x60;GET /v1/accounts&#x60;). | 
**AdAccountId** | **string** | Platform ad account ID, from &#x60;GET /v1/ads/accounts&#x60;. | 
**Level** | **AdRuleLevel** |  | 
**CampaignIds** | **List&lt;string&gt;** | Only check these platform campaign IDs (or their ad sets). Leave out to check the whole ad account. | [optional] 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Actions** | [**List&lt;AdRuleAction&gt;**](AdRuleAction.md) | Each type at most once, and at most one of &#x60;pause&#x60;, &#x60;activate&#x60; and &#x60;adjust_budget&#x60;. | 
**Schedule** | [**AdRuleSchedule**](AdRuleSchedule.md) | Leave it out to run every 60 minutes. | [optional] 
**CooldownMinutes** | **int** | How long the rule leaves an object alone after acting on it. | [optional] [default to 1440]
**Enabled** | **bool** |  | [optional] [default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

