# Zernio.Model.UpdateAdRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Level** | **AdRuleLevel** |  | [optional] 
**CampaignIds** | **List&lt;string&gt;** |  | [optional] 
**Filters** | [**List&lt;AdRuleFiltersInner&gt;**](AdRuleFiltersInner.md) | Narrows the objects the rule checks. Every filter must hold. Text compares without case, and a missing field reads as empty. | [optional] 
**Lifecycle** | [**AdRuleLifecycle**](AdRuleLifecycle.md) |  | [optional] 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | [optional] 
**Actions** | [**List&lt;AdRuleAction&gt;**](AdRuleAction.md) | Each type at most once, and at most one of &#x60;pause&#x60;, &#x60;activate&#x60;, &#x60;adjust_budget&#x60;, &#x60;adjust_bid&#x60;, &#x60;duplicate&#x60; and &#x60;edit_name&#x60;. | [optional] 
**Schedule** | [**AdRuleSchedule**](AdRuleSchedule.md) |  | [optional] 
**CooldownMinutes** | **int** |  | [optional] 
**Enabled** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

