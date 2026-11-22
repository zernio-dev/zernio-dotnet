# Zernio.Model.FlowAutomationDefinition
A flow: the workflow builder's graph of steps on one messaging account, the same flow `/v1/workflows` serves (versions and activation rules included). Its `kind` is `workflow`. Unknown fields are refused.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Status** | **string** | A new flow is &#x60;draft&#x60; (the default) or &#x60;active&#x60;, which needs a complete graph. An active or paused flow never goes back to draft, and only an active flow can be paused. | [optional] 
**Trigger** | [**FlowAutomationDefinitionTrigger**](FlowAutomationDefinitionTrigger.md) |  | 
**Graph** | [**FlowAutomationDefinitionGraph**](FlowAutomationDefinitionGraph.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

