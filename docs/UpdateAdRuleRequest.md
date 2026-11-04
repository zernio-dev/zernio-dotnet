# Zernio.Model.UpdateAdRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Level** | **AdRuleLevel** |  | [optional] 
**CampaignIds** | **List&lt;string&gt;** |  | [optional] 
**Filters** | [**List&lt;AdRuleFiltersInner&gt;**](AdRuleFiltersInner.md) | Narrows the objects the rule checks. Every filter must hold. A campaign rule reads &#x60;name&#x60;, &#x60;campaign_id&#x60;, &#x60;goal&#x60;, &#x60;days_live&#x60; and &#x60;budget_level&#x60;; an ad set rule also &#x60;campaign_name&#x60; and &#x60;adset_id&#x60;; an ad rule also &#x60;adset_name&#x60; and &#x60;ad_id&#x60;. | [optional] 
**Groups** | [**List&lt;AdRuleGroupsInner&gt;**](AdRuleGroupsInner.md) | Null removes the groups; each campaign is then judged on its own. | [optional] 
**Lifecycle** | [**AdRuleLifecycle**](AdRuleLifecycle.md) |  | [optional] 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | [optional] 
**Actions** | [**List&lt;AdRuleAction&gt;**](AdRuleAction.md) | Each type at most once, and at most one of &#x60;pause&#x60;, &#x60;activate&#x60;, &#x60;adjust_budget&#x60;, &#x60;adjust_bid&#x60;, &#x60;duplicate&#x60; and &#x60;edit_name&#x60;. | [optional] 
**Schedule** | [**AdRuleSchedule**](AdRuleSchedule.md) |  | [optional] 
**CooldownMinutes** | **int** |  | [optional] 
**Enabled** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

