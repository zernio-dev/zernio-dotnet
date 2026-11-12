# Zernio.Model.AdRuleEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EvaluatedAt** | **DateTime** |  | 
**Today** | **DateOnly** | The ad account&#39;s calendar date the windows were resolved against. | 
**Timezone** | **string** | IANA timezone of the ad account. | 
**TimezoneAssumed** | **bool** | True when the ad account has no known timezone and UTC was assumed. | 
**Currency** | **string** |  | 
**HourlyThrough** | **DateTime?** | Where the hourly windows (&#x60;last_complete_hour&#x60;, &#x60;last_3h&#x60;, &#x60;today_so_far&#x60;) ended: the end of the latest hour a sync has settled. Null when the rule has none or they could not be read. | [optional] 
**Matched** | **int** | How many objects meet every condition. | 
**Objects** | [**List&lt;AdRuleObjectEvaluation&gt;**](AdRuleObjectEvaluation.md) | Every delivering campaign or ad set in scope (for an &#x60;activate&#x60; rule, the rule-paused ones it may reactivate). | 
**Groups** | [**List&lt;AdRuleEvaluationGroupsInner&gt;**](AdRuleEvaluationGroupsInner.md) | Each group&#39;s totals, for a rule with groups. Null otherwise. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

