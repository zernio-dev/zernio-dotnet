# Zernio.Model.AutomationGraph
An automation's definition as one graph: the trigger that starts it, the nodes its runs walk from `entry` along `edges`, and its guardrails. Ad rules, event and scheduled automations and sequences run their nodes in one chain, a condition first where the kind has one.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Triggers** | [**List&lt;AutomationGraphTriggersInner&gt;**](AutomationGraphTriggersInner.md) | One trigger. Its &#x60;type&#x60; is the kind&#39;s &#x60;trigger.type&#x60;; &#x60;config&#x60; holds the rest of the trigger, and &#x60;subjects&#x60; for a schedule. | 
**Nodes** | [**List&lt;AutomationGraphNodesInner&gt;**](AutomationGraphNodesInner.md) |  | 
**Edges** | [**List&lt;AutomationGraphEdgesInner&gt;**](AutomationGraphEdgesInner.md) |  | 
**Entry** | **List&lt;string&gt;** | The node runs start at. | 
**Limits** | [**AutomationGraphLimits**](AutomationGraphLimits.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

