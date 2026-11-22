# Zernio.Model.SequenceAutomationDefinition
Messages a contact over time from one account, starting when the contact is enrolled (`POST /v1/sequences/{sequenceId}/enroll`, a flow, or by hand). The same sequence `/v1/sequences` serves. Unknown fields are refused.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Status** | **string** | A new sequence is on unless &#x60;draft&#x60;. A draft can be activated; a sequence that ran can only be paused and activated again. | [optional] [default to StatusEnum.Active]
**Trigger** | [**SequenceAutomationDefinitionTrigger**](SequenceAutomationDefinitionTrigger.md) |  | 
**Steps** | [**List&lt;AutomationSequenceStep&gt;**](AutomationSequenceStep.md) | At least one step for an active sequence. Steps change only while it is a draft or paused. | 
**Limits** | [**SequenceAutomationDefinitionLimits**](SequenceAutomationDefinitionLimits.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

