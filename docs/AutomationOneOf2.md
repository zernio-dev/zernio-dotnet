# Zernio.Model.AutomationOneOf2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** |  | 
**Trigger** | [**AutomationPostSchedule**](AutomationPostSchedule.md) |  | 
**Subjects** | [**AutomationPostSubjects**](AutomationPostSubjects.md) |  | 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 
**Steps** | [**List&lt;ScheduledAutomationDefinitionStepsInner&gt;**](ScheduledAutomationDefinitionStepsInner.md) |  | 
**Limits** | [**AutomationEventLimits**](AutomationEventLimits.md) |  | [optional] 
**Id** | **string** |  | 
**Kind** | **string** |  | 
**VarVersion** | **string** | Send it back as &#x60;If-Match&#x60; when editing, so an edit made after someone else saved is refused. | 
**LastCheckAt** | **DateTime** | Null until an ad rule first checks. Always null for event and scheduled automations; their checks list when they ran. | 
**NextCheckAt** | **DateTime** | Null while paused. Always null for event and scheduled automations. | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**Template** | [**AutomationRecordTemplate**](AutomationRecordTemplate.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

