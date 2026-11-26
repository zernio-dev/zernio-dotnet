# Zernio.Model.CreateAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** |  | [optional] 
**Trigger** | [**FlowAutomationDefinitionTrigger**](FlowAutomationDefinitionTrigger.md) |  | 
**Subjects** | [**AutomationPostSubjects**](AutomationPostSubjects.md) |  | 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Alert** | [**AutomationAlert**](AutomationAlert.md) |  | [optional] 
**Steps** | [**List&lt;AutomationSequenceStep&gt;**](AutomationSequenceStep.md) | At least one step for an active sequence. Steps change only while it is a draft or paused. | 
**Limits** | [**CommentAutomationDefinitionLimits**](CommentAutomationDefinitionLimits.md) |  | 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 
**Description** | **string** | Sequences. | [optional] 
**OrTriggers** | [**List&lt;CommentAutomationDefinitionOrTriggersInner&gt;**](CommentAutomationDefinitionOrTriggersInner.md) | A DM with the same keywords also starts it (&#x60;dm.keyword&#x60;), at the decision and with no comment to act on. Comment triggers with keywords only. | [optional] 
**Graph** | [**AutomationGraph**](AutomationGraph.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

