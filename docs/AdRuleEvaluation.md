# Zernio.Model.AdRuleEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EvaluatedAt** | **DateTime** |  | 
**Today** | **DateOnly** | The ad account&#39;s calendar date the windows were resolved against. | 
**Timezone** | **string** | IANA timezone of the ad account. | 
**TimezoneAssumed** | **bool** | True when the ad account has no known timezone and UTC was assumed. | 
**Currency** | **string** |  | 
**Matched** | **int** | How many objects meet every condition. | 
**Objects** | [**List&lt;AdRuleObjectEvaluation&gt;**](AdRuleObjectEvaluation.md) | Every delivering campaign or ad set in scope (for an &#x60;activate&#x60; rule, the rule-paused ones it may reactivate). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

