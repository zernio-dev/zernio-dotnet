# Zernio.Model.SubmitFeedbackRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | What kind of feedback this is. | 
**Summary** | **string** | One line describing the problem or the missing capability. Also the dedup key. | 
**Details** | **string** | Longer explanation: what you were trying to do, steps to reproduce, the use case. | [optional] 
**Endpoint** | **string** | The endpoint involved, e.g. &#x60;POST /v1/posts&#x60;. | [optional] 
**RequestId** | **string** | The &#x60;x-request-id&#x60; header of the failing response, if any. | [optional] 
**Expected** | **string** | What you expected to happen. | [optional] 
**Actual** | **string** | What actually happened, e.g. the error message. | [optional] 
**Agent** | [**SubmitFeedbackRequestAgent**](SubmitFeedbackRequestAgent.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

