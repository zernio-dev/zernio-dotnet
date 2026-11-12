# Zernio.Model.EventAutomationDefinition
Runs when something happens in Zernio, such as a post failing, and notifies. Unknown fields are refused.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Status** | **string** | A new event automation is on unless &#x60;paused&#x60;. | [optional] [default to StatusEnum.Active]
**Trigger** | [**AutomationEventTrigger**](AutomationEventTrigger.md) |  | 
**Steps** | [**List&lt;AutomationNotifyStep&gt;**](AutomationNotifyStep.md) | May be empty: an automation with no steps only records each event it matches as a check with outcome &#x60;triggered&#x60; and no action. &#x60;limits.cooldown&#x60; and &#x60;limits.maxChangesPerDay&#x60; count actions, so they do nothing for it. | 
**Limits** | [**AutomationEventLimits**](AutomationEventLimits.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

