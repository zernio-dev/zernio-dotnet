# Zernio.Model.AdRuleObjectEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform ID of the campaign, ad set or ad. A keyword is &#x60;{adGroupId}~{criterionId}&#x60;, a search term &#x60;{campaignId}~{term}&#x60;. | 
**Name** | **string** | The object&#39;s name: the keyword text or the search term. | 
**CampaignId** | **string** |  | 
**CampaignName** | **string** | Absent on runs recorded before November 2026. | [optional] 
**Matched** | **bool** | True when every condition holds. | 
**Group** | **string** | For a rule with groups: the group this campaign was judged in. &#x60;matched&#x60; and &#x60;conditions&#x60; are the group&#39;s. | [optional] 
**Conditions** | [**List&lt;AdRuleObjectEvaluationConditionsInner&gt;**](AdRuleObjectEvaluationConditionsInner.md) |  | 
**Readings** | [**List&lt;AdRuleObjectEvaluationReadingsInner&gt;**](AdRuleObjectEvaluationReadingsInner.md) | On a matched object: spend, impressions and clicks over each window its conditions read, and the other search impression shares when a condition reads one. Left out where a condition already reads the value. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

