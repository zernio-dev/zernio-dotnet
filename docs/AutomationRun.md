# Zernio.Model.AutomationRun
One subject going through an automation, the same shape for every kind. A flow, sequence or comment to DM run is one conversation, contact or comment; an ad rule, event or scheduled automation run is one check that acted or tried to.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**AutomationId** | **string** |  | 
**Kind** | **string** |  | 
**Status** | **string** | &#x60;live&#x60; while it runs or waits (a comment to DM run waiting for its follow gate is live). | 
**Subject** | [**AutomationRunSubject**](AutomationRunSubject.md) |  | 
**StartedAt** | **DateTime** |  | 
**EndedAt** | **DateTime?** |  | 
**ExitReason** | **string** | Why an exited or failed run stopped, for example &#x60;handoff&#x60; (a flow handed the conversation to a person), &#x60;wait_expired&#x60;, &#x60;superseded&#x60;, &#x60;replied&#x60;, &#x60;unsubscribed&#x60; or &#x60;skipped&#x60;. | 
**Error** | **string** |  | 
**Steps** | [**AutomationRunSteps**](AutomationRunSteps.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

