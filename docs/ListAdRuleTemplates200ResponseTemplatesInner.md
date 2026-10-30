# Zernio.Model.ListAdRuleTemplates200ResponseTemplatesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Name** | **string** |  | 
**Description** | **string** |  | 
**Level** | **AdRuleLevel** |  | 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Actions** | [**List&lt;AdRuleAction&gt;**](AdRuleAction.md) | Each type at most once, and at most one of &#x60;pause&#x60;, &#x60;activate&#x60; and &#x60;adjust_budget&#x60;. | 
**Schedule** | [**AdRuleSchedule**](AdRuleSchedule.md) |  | 
**CooldownMinutes** | **int** |  | 
**Platforms** | **List&lt;string&gt;** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

