# Zernio.Model.AdRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Name** | **string** |  | 
**AccountId** | **string** | The ads connection the rule acts through. | 
**Platform** | **string** | Ad platform, for example &#x60;facebook&#x60; (Meta) or &#x60;google&#x60;. | 
**AdAccountId** | **string** | Platform ad account ID. | 
**Level** | **AdRuleLevel** |  | 
**CampaignIds** | **List&lt;string&gt;** | Platform campaign IDs the rule is limited to. Null checks the whole ad account. | 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Actions** | [**List&lt;AdRuleAction&gt;**](AdRuleAction.md) | Each type at most once, and at most one of &#x60;pause&#x60;, &#x60;activate&#x60; and &#x60;adjust_budget&#x60;. | 
**Schedule** | [**AdRuleSchedule**](AdRuleSchedule.md) |  | 
**CooldownMinutes** | **int** |  | 
**Enabled** | **bool** |  | 
**LastRunAt** | **DateTime?** |  | 
**NextRunAt** | **DateTime?** | Null while the rule is disabled. | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

