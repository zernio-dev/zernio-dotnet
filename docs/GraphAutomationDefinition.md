# Zernio.Model.GraphAutomationDefinition
Any automation sent as an automation graph. It is saved as its own shape would be.  - A comment to DM keeps its fixed node ids (`dm`, `reply`, `like`, `hide`, `delay`, ...) and may carry its DM door as a second trigger with its own `entry`. - A flow's trigger settings go on its trigger node, added when the graph has none. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Description** | **string** | Sequences and flows. | [optional] 
**Status** | **string** |  | [optional] 
**Graph** | [**AutomationGraph**](AutomationGraph.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

