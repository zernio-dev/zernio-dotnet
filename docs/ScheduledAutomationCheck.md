# Zernio.Model.ScheduledAutomationCheck
One check of a scheduled automation.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AutomationId** | **string** |  | 
**CheckedAt** | **DateTime** |  | 
**Outcome** | **string** | &#x60;paused&#x60;: the team used its free automation runs with no payment method on file, so the check did not run. &#x60;error&#x60; says why. | 
**Evaluated** | **int** | Posts judged. | 
**AnalyticsSyncedAt** | **DateTime?** | The oldest analytics sync among the posts judged: their numbers are as of then. | 
**Matched** | [**List&lt;ScheduledAutomationCheckMatchedInner&gt;**](ScheduledAutomationCheckMatchedInner.md) | Up to 20 matching posts. | 
**Actions** | [**List&lt;ScheduledAutomationCheckActionsInner&gt;**](ScheduledAutomationCheckActionsInner.md) |  | 
**Error** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

