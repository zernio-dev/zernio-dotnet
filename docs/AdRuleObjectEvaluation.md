# Zernio.Model.AdRuleObjectEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform ID of the campaign or ad set. | 
**Name** | **string** |  | 
**CampaignId** | **string** |  | 
**Matched** | **bool** | True when every condition holds. | 
**Group** | **string** | For a rule with groups: the group this campaign was judged in. &#x60;matched&#x60; and &#x60;conditions&#x60; are the group&#39;s. | [optional] 
**Conditions** | [**List&lt;AdRuleObjectEvaluationConditionsInner&gt;**](AdRuleObjectEvaluationConditionsInner.md) |  | 
**Readings** | [**List&lt;AdRuleObjectEvaluationReadingsInner&gt;**](AdRuleObjectEvaluationReadingsInner.md) | On a matched object: spend, impressions and clicks over each window its conditions read, and the other search impression shares when a condition reads one. Left out where a condition already reads the value. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

