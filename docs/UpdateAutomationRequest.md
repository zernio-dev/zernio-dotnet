# Zernio.Model.UpdateAutomationRequest
Any top-level field of the automation's kind (see `AutomationDefinition`); the fields of another kind are refused.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Description** | **string** | Sequences and flows. | [optional] 
**Status** | **string** | &#x60;draft&#x60; only for a sequence or a flow that has not left draft. | [optional] 
**Trigger** | **Object** | The trigger of the automation&#39;s kind. | [optional] 
**OrTriggers** | **List&lt;Object&gt;** | Comment to DM. | [optional] 
**Graph** | **Object** | An &#x60;AutomationGraph&#x60; (with &#x60;triggers&#x60;) replaces the whole definition of any kind, sent without &#x60;trigger&#x60;, &#x60;orTriggers&#x60;, &#x60;subjects&#x60;, &#x60;filter&#x60;, &#x60;conditions&#x60;, &#x60;alert&#x60;, &#x60;steps&#x60; or &#x60;limits&#x60;. Comment to DM and flows also take their own graph, as read. | [optional] 
**Subjects** | [**UpdateAutomationRequestSubjects**](UpdateAutomationRequestSubjects.md) |  | [optional] 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 
**Conditions** | [**AdRuleConditions**](AdRuleConditions.md) |  | [optional] 
**Alert** | [**AutomationAlert**](AutomationAlert.md) |  | [optional] 
**Steps** | [**List&lt;UpdateAutomationRequestStepsInner&gt;**](UpdateAutomationRequestStepsInner.md) | The steps the automation&#39;s kind takes. | [optional] 
**Limits** | **Object** | The limits of the automation&#39;s kind. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

