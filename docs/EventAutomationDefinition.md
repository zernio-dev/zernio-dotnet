# Zernio.Model.EventAutomationDefinition
Runs when something happens in Zernio, such as a post failing, and notifies. Unknown fields are refused.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** | A new event automation is on unless &#x60;paused&#x60;. | [optional] [default to StatusEnum.Active]
**Trigger** | [**AutomationEventTrigger**](AutomationEventTrigger.md) |  | 
**Steps** | [**List&lt;AutomationNotifyStep&gt;**](AutomationNotifyStep.md) |  | 
**Limits** | [**AutomationEventLimits**](AutomationEventLimits.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

