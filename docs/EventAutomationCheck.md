# Zernio.Model.EventAutomationCheck
One event that reached an event automation.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AutomationId** | **string** |  | 
**CheckedAt** | **DateTime** |  | 
**Outcome** | **string** |  | 
**Evaluated** | **int** |  | 
**Event** | **string** |  | 
**EventId** | **string** |  | 
**Subject** | [**EventAutomationCheckSubject**](EventAutomationCheckSubject.md) |  | 
**Filter** | [**List&lt;AutomationFactResult&gt;**](AutomationFactResult.md) |  | 
**Actions** | [**List&lt;AutomationRunResult&gt;**](AutomationRunResult.md) |  | 
**Error** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

