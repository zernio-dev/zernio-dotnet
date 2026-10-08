# Zernio.Model.CreateSupportRunRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** | The question. Leading and trailing whitespace is trimmed. | 
**ThreadId** | **string** | Continue this thread. The thread must have a run started by your team, and no run in progress. | [optional] 
**Context** | [**CreateSupportRunRequestContext**](CreateSupportRunRequestContext.md) |  | [optional] 
**MaxCostUsd** | **decimal** | Cost cap for this run, in USD. The run stops at the cap and bills at most this amount. | [optional] [default to 3M]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

