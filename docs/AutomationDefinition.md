# Zernio.Model.AutomationDefinition
An automation of one of six kinds. The kind follows from `trigger.type`, each type belonging to one kind; a `schedule` is an ad rule unless `subjects.each` is `post`, and a flow may leave `trigger.type` out:  - **Ad rule**: a `schedule` trigger over campaigns, ad sets, ads, Google keywords or Google search terms, with metric `conditions` and ad `steps`. - **Event**: a Zernio event in `trigger.type`, narrowed by `trigger.filter`, with notify steps, or none to only record each matching event as a check. - **Scheduled**: a `schedule` trigger over `subjects.each: post`, narrowed by `filter`, with notify and boost steps. - **Sequence**: an `enrollment` trigger on one account, with message steps sent over time. - **Comment to DM**: a comment door in `trigger.type` (`comment.keyword`, `comment.live`, `story.reply`, `story.mention`) with a `graph`. - **Flow**: a workflow trigger (`inbound_message`, `api_call`, `comment` and the others) with the builder's `graph`; `trigger.type` may be left out, read from the graph's trigger node. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** | A new flow is &#x60;draft&#x60; (the default) or &#x60;active&#x60;, which needs a complete graph. An active or paused flow never goes back to draft, and only an active flow can be paused. | [optional] 
**Trigger** | [**FlowAutomationDefinitionTrigger**](FlowAutomationDefinitionTrigger.md) |  | 
**Subjects** | [**AutomationPostSubjects**](AutomationPostSubjects.md) |  | 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | 
**Alert** | [**AutomationAlert**](AutomationAlert.md) |  | [optional] 
**Steps** | [**List&lt;AutomationSequenceStep&gt;**](AutomationSequenceStep.md) | At least one step for an active sequence. Steps change only while it is a draft or paused. | 
**Limits** | [**CommentAutomationDefinitionLimits**](CommentAutomationDefinitionLimits.md) |  | 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 
**Description** | **string** |  | [optional] 
**OrTriggers** | [**List&lt;CommentAutomationDefinitionOrTriggersInner&gt;**](CommentAutomationDefinitionOrTriggersInner.md) | A DM with the same keywords also starts it (&#x60;dm.keyword&#x60;), at the decision and with no comment to act on. Comment triggers with keywords only. | [optional] 
**Graph** | [**FlowAutomationDefinitionGraph**](FlowAutomationDefinitionGraph.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

