# Zernio.Model.AutomationDefinition
An automation of one of three kinds, told apart by its shape:  - **Ad rule**: a `schedule` trigger over campaigns, ad sets or ads, with metric `conditions` and ad `steps`. - **Event**: a Zernio event in `trigger.type`, narrowed by `trigger.filter`, with notify steps. - **Scheduled**: a `schedule` trigger over `subjects.each: post`, narrowed by `filter`, with notify and boost steps. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** | A new scheduled automation is on unless &#x60;paused&#x60;. | [optional] [default to StatusEnum.Active]
**Trigger** | [**AutomationPostSchedule**](AutomationPostSchedule.md) |  | 
**Subjects** | [**AutomationPostSubjects**](AutomationPostSubjects.md) |  | 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Alert** | [**AutomationAlert**](AutomationAlert.md) |  | [optional] 
**Steps** | [**List&lt;ScheduledAutomationDefinitionStepsInner&gt;**](ScheduledAutomationDefinitionStepsInner.md) |  | 
**Limits** | [**AutomationEventLimits**](AutomationEventLimits.md) |  | [optional] 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

