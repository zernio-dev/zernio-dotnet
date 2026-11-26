# Zernio.Model.Automation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** | Only a sequence or a flow can be a draft. | 
**Trigger** | [**FlowAutomationDefinitionTrigger**](FlowAutomationDefinitionTrigger.md) |  | 
**Subjects** | [**AutomationPostSubjects**](AutomationPostSubjects.md) |  | 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Alert** | [**AutomationAlert**](AutomationAlert.md) |  | [optional] 
**Steps** | [**List&lt;AutomationSequenceStep&gt;**](AutomationSequenceStep.md) | At least one step for an active sequence. Steps change only while it is a draft or paused. | 
**Limits** | [**CommentAutomationDefinitionLimits**](CommentAutomationDefinitionLimits.md) |  | 
**Id** | **string** |  | 
**Kind** | **string** |  | 
**VarVersion** | **string** | Send it back as &#x60;If-Match&#x60; when editing, so an edit made after someone else saved is refused. | 
**LastCheckAt** | **DateTime** | Null until an ad rule first checks. Always null for every other kind; the checks of event and scheduled automations list when they ran. | 
**NextCheckAt** | **DateTime** | Null while paused. Always null for every kind but ad rules. | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**Template** | [**AutomationRecordTemplate**](AutomationRecordTemplate.md) |  | [optional] 
**Graph** | [**FlowAutomationDefinitionGraph**](FlowAutomationDefinitionGraph.md) |  | 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 
**Description** | **string** |  | [optional] 
**Platform** | **string** | The account&#39;s platform. | 
**Enrollments** | [**AutomationOneOf3AllOfEnrollments**](AutomationOneOf3AllOfEnrollments.md) |  | 
**OrTriggers** | [**List&lt;CommentAutomationDefinitionOrTriggersInner&gt;**](CommentAutomationDefinitionOrTriggersInner.md) | A DM with the same keywords also starts it (&#x60;dm.keyword&#x60;), at the decision and with no comment to act on. Comment triggers with keywords only. | [optional] 
**ReadOnly** | **bool** | Always true when present. Present when the graph only comes near what the automation does. It is read here and edited through &#x60;/v1/comment-automations&#x60;; an edit here is refused. | [optional] 
**Stats** | [**AutomationOneOf4AllOfStats**](AutomationOneOf4AllOfStats.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

