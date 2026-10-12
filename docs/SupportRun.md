# Zernio.Model.SupportRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RunId** | **string** | Run id, a 24-character hex string. | 
**ThreadId** | **string** | Conversation thread id. Send it back as &#x60;threadId&#x60; to ask a follow-up in the same thread. | 
**Status** | **string** | queued and running are in progress. needs_human means Ana handed the question to a person instead of answering; when &#x60;supportTicket&#x60; is set, a Zernio teammate has been notified and will follow up by email. | 
**StopReason** | **string** | Why the run stopped. Null while it is in progress. | 
**Answer** | **string** | Ana&#39;s answer. Null while the run is in progress or when it failed. | 
**Usage** | [**SupportRunUsage**](SupportRunUsage.md) |  | 
**CostUsd** | **decimal** | The exact amount charged for the question, in USD, never above &#x60;maxCostUsd&#x60;. 0 for a failed run. | 
**MaxCostUsd** | **decimal** | The cost cap this run was started with, in USD. | 
**CreatedAt** | **DateTime** |  | 
**StartedAt** | **DateTime?** |  | 
**FinishedAt** | **DateTime?** |  | 
**SupportTicket** | [**SupportRunSupportTicket**](SupportRunSupportTicket.md) |  | 
**PollAfterSeconds** | **int** | Seconds to wait before polling again. Present only while the run is queued or running. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

