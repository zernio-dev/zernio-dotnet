# Zernio.Model.ScheduledAutomationDefinition
Checks a profile's recent posts on a schedule. Each post that matches `filter` is notified about, and can be boosted. At most 20 posts are acted on per check. Unknown fields are refused. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** | A new scheduled automation is on unless &#x60;paused&#x60;. | [optional] [default to StatusEnum.Active]
**Trigger** | [**AutomationPostSchedule**](AutomationPostSchedule.md) |  | 
**Subjects** | [**AutomationPostSubjects**](AutomationPostSubjects.md) |  | 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 
**Steps** | [**List&lt;ScheduledAutomationDefinitionStepsInner&gt;**](ScheduledAutomationDefinitionStepsInner.md) |  | 
**Limits** | [**AutomationEventLimits**](AutomationEventLimits.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

