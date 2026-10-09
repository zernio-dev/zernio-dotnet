# Zernio.Model.WebhookPayloadWorkflowRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Id** | **string** | Event id, the dedupe key. | 
**Event** | **string** |  | 
**Timestamp** | **DateTime** |  | 
**Workflow** | [**WebhookPayloadWorkflowRunWorkflow**](WebhookPayloadWorkflowRunWorkflow.md) |  | 
**Execution** | [**WebhookPayloadWorkflowRunExecution**](WebhookPayloadWorkflowRunExecution.md) |  | 
**Conversation** | [**WebhookPayloadWorkflowRunConversation**](WebhookPayloadWorkflowRunConversation.md) |  | 
**Contact** | [**WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**Trigger** | [**WebhookPayloadWorkflowRunTrigger**](WebhookPayloadWorkflowRunTrigger.md) |  | 
**Error** | **string** | workflow.run.failed only: which node failed and why. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

