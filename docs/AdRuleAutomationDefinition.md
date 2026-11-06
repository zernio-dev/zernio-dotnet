# Zernio.Model.AdRuleAutomationDefinition
An ad rule. It is also readable under `/v1/ads/rules` with the same id. Unknown fields are refused.  To have a person OK each change before it is made, put an `approval.request` step before the `ads.*` step. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** | A new ad rule stays paused unless &#x60;active&#x60;. | [optional] [default to StatusEnum.Paused]
**Trigger** | [**AutomationScheduleTrigger**](AutomationScheduleTrigger.md) |  | 
**Subjects** | [**AutomationSubjects**](AutomationSubjects.md) |  | 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Alert** | [**AutomationAlert**](AutomationAlert.md) |  | [optional] 
**Steps** | [**List&lt;AutomationStep&gt;**](AutomationStep.md) |  | 
**Limits** | [**AutomationLimits**](AutomationLimits.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

