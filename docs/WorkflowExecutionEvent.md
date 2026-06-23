# Zernio.Model.WorkflowExecutionEvent
One entry in a workflow execution's timeline. Emitted by the executor on every node visit and lifecycle transition, surfaced by `GET /v1/workflows/{workflowId}/executions/ {executionId}/events` for run inspection in the Runs UI. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Action** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**NodeId** | **string** | Present on &#x60;node_*&#x60; events | [optional] 
**NodeType** | **string** | Present on &#x60;node_*&#x60; events | [optional] 
**SourceHandle** | **string** | The edge handle the executor followed out of this node (see &#x60;WorkflowEdge.sourceHandle&#x60;) | [optional] 
**DurationMs** | **int?** | Node run time; present on &#x60;node_completed&#x60; and &#x60;node_failed&#x60; | [optional] 
**ErrorMessage** | **string** | Failure detail; present on &#x60;node_failed&#x60; and &#x60;execution_exited&#x60; | [optional] 
**Meta** | **Dictionary&lt;string, Object&gt;** | Per-node-type payload. Shape varies — see WorkflowNode &#x60;type&#x60;. Examples:   &#x60;send_message&#x60; → &#x60;{ messageType, text, recipient }&#x60;,   &#x60;webhook&#x60; → &#x60;{ url, method, statusCode, responseTimeMs, responsePreview }&#x60;,   &#x60;ai&#x60; → &#x60;{ model, provider, inputTokens, outputTokens, responsePreview }&#x60;,   &#x60;condition&#x60; → &#x60;{ matchedHandle, rulesEvaluated }&#x60;,   &#x60;a_b_split&#x60; → &#x60;{ percentage, chosen }&#x60;.  | [optional] 
**At** | **DateTime** | Event timestamp (UTC) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

