# Zernio.Model.WebhookPayloadAutomationCheckCompletedCheck

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Slot** | **DateTime** | The scheduled time the check ran for. | 
**Outcome** | **string** | &#x60;paused&#x60;: the team used its free automation runs with no payment method on file, so the check did not run. &#x60;error&#x60; says why. | 
**SubjectsEvaluated** | **int** | How many objects the check read. | 
**ActionsCount** | **int** | How many actions it recorded. | 
**Error** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

