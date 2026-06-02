# Zernio.Model.CreateWorkflowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**AccountId** | **string** |  | 
**Platform** | **string** |  | [optional] [default to PlatformEnum.Whatsapp]
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Nodes** | [**List&lt;WorkflowNode&gt;**](WorkflowNode.md) |  | [optional] 
**Edges** | [**List&lt;WorkflowEdge&gt;**](WorkflowEdge.md) |  | [optional] 
**EntryNodeId** | **string** | The trigger node id; derived from the single trigger node if omitted | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

