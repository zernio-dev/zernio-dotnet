# Zernio.Model.AutomationRunDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AutomationId** | **string** |  | 
**Kind** | **string** |  | 
**Status** | **string** | &#x60;live&#x60; while it runs or waits (a comment to DM run waiting for its follow gate is live). | 
**Subject** | [**AutomationRunSubject**](AutomationRunSubject.md) |  | 
**StartedAt** | **DateTime** |  | 
**EndedAt** | **DateTime** |  | 
**ExitReason** | **string** | Why an exited or failed run stopped, for example &#x60;replied&#x60;, &#x60;unsubscribed&#x60; or &#x60;skipped&#x60;. | 
**Error** | **string** |  | 
**Steps** | [**AutomationRunSteps**](AutomationRunSteps.md) |  | 
**Trace** | [**List&lt;AutomationRunDetailAllOfTrace&gt;**](AutomationRunDetailAllOfTrace.md) | Each step in order. Null where the run&#39;s store keeps no step by step record (runs on the automation engine keep where they are and how many steps they took). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

