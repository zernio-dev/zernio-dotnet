# Zernio.Model.AdRuleAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Send the &#x60;ad_rule.triggered&#x60; webhook, and the alert to every &#x60;send&#x60; destination. | 
**Send** | [**List&lt;AdRuleActionOneOfSendInner&gt;**](AdRuleActionOneOfSendInner.md) | Also send a short alert through accounts you connected: what matched, the values and what the rule did. Up to 5 destinations, checked when the rule is saved.  A destination that fails is reported in the run&#39;s &#x60;notification&#x60;; it never undoes a change.  | [optional] 
**MaxChangesPerDay** | **int** | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with &#x60;daily_limit_reached&#x60; and tried again later. | [optional] 
**MaxChangesPerObject** | **int** | At most this many changes to one object by this rule, counted over the last 400 days. An object at the limit is left alone like one in cooldown. | [optional] 
**IncludeManuallyPaused** | **bool** | Also reactivate paused objects that no rule paused, as soon as they match. | [optional] 
**Status** | **string** | How the copy starts. Defaults to &#x60;paused&#x60;. | [optional] 
**RenameSuffix** | **string** | Text added to the copy&#39;s name. | [optional] 
**Amount** | **decimal** | The daily budget to set, in the ad account currency. An object already at it is skipped with &#x60;already_at_amount&#x60;. | 
**Direction** | **string** |  | 
**Percent** | **int** | Change in percent: up to 100 for an increase, up to 90 for a decrease. | 
**Limit** | **decimal** | The budget never goes above this on an increase, or below it on a decrease, in the ad account currency. | 
**Target** | **string** | Which target moves: &#x60;cpa&#x60; in the ad account currency, &#x60;roas&#x60; as a ratio (3 is 300%). | 
**Metric** | **string** | What objects are ranked by: any condition metric except &#x60;day_of_month&#x60; and &#x60;working_day_of_month&#x60;, or a result metric (&#x60;result:&lt;key&gt;&#x60;) on campaign rules.  Objects without a value are not ranked, except one that spent with no result on a metric where lower is best (a CPA with no conversions): it ranks worst and only gives. | 
**Window** | **string** | The period the metric is read over, like a condition window. | 
**Best** | **string** | Which end of the ranking is best. Defaults to &#x60;lowest&#x60; for &#x60;cpa&#x60;, &#x60;cpc&#x60;, &#x60;cpm&#x60;, &#x60;frequency&#x60; and result metrics whose formula has spend above the line (cost per sale, %CAC), &#x60;highest&#x60; otherwise. | [optional] 
**From** | [**AdRuleActionOneOf6From**](AdRuleActionOneOf6From.md) |  | 
**To** | [**AdRuleActionOneOf6To**](AdRuleActionOneOf6To.md) |  | 
**MinBudget** | **decimal** | A giver never goes below this daily budget. A giver also always keeps a tenth of its budget. | [optional] 
**MaxBudget** | **decimal** | A receiver never goes above this daily budget; what receivers cannot take stays with the givers. | [optional] 
**Add** | **string** | Text to add, like &#x60;[WINNER]&#x60;. Compared without case. | [optional] 
**At** | **string** | Where &#x60;add&#x60; goes. Defaults to &#x60;start&#x60;. | [optional] 
**Remove** | **string** | Text to take out of the name, every copy of it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

