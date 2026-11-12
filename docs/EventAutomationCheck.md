# Zernio.Model.EventAutomationCheck
One event that reached an event automation.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AutomationId** | **string** |  | 
**CheckedAt** | **DateTime** |  | 
**Outcome** | **string** | &#x60;paused&#x60;: the team used its free automation runs with no payment method on file, so the check did not run. &#x60;error&#x60; says why. | 
**Evaluated** | **int** |  | 
**Event** | **string** |  | 
**EventId** | **string** |  | 
**Subject** | [**EventAutomationCheckSubject**](EventAutomationCheckSubject.md) |  | 
**Facts** | **Dictionary&lt;string, Object&gt;** | The event&#39;s facts as the trigger read them, keyed by fact name. Recorded only for an automation with no steps (one that only records each event).  Null for an automation with steps, whose filter results show the facts it compared, and on checks recorded before facts were kept. Content facts are null for a team that keeps no content. | 
**Filter** | [**List&lt;AutomationFactResult&gt;**](AutomationFactResult.md) |  | 
**Actions** | [**List&lt;AutomationRunResult&gt;**](AutomationRunResult.md) |  | 
**Error** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

