# Zernio.Model.AutomationCheck
One check, shaped by the automation's kind.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AutomationId** | **string** |  | 
**CheckedAt** | **DateTime** |  | 
**Outcome** | **string** |  | 
**Evaluated** | **int** | Posts judged. | 
**Subjects** | [**List&lt;AdRuleAutomationCheckSubjectsInner&gt;**](AdRuleAutomationCheckSubjectsInner.md) |  | 
**Actions** | [**List&lt;ScheduledAutomationCheckActionsInner&gt;**](ScheduledAutomationCheckActionsInner.md) |  | 
**Notification** | [**AdRuleAutomationCheckNotification**](AdRuleAutomationCheckNotification.md) |  | 
**Error** | **string** |  | 
**Event** | **string** |  | 
**EventId** | **string** |  | 
**Subject** | [**EventAutomationCheckSubject**](EventAutomationCheckSubject.md) |  | 
**Filter** | [**List&lt;AutomationFactResult&gt;**](AutomationFactResult.md) |  | 
**AnalyticsSyncedAt** | **DateTime** | The oldest analytics sync among the posts judged: their numbers are as of then. | 
**Matched** | [**List&lt;ScheduledAutomationCheckMatchedInner&gt;**](ScheduledAutomationCheckMatchedInner.md) | Up to 20 matching posts. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

