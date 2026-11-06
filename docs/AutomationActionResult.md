# Zernio.Model.AutomationActionResult
What an ad rule did to one object, as an absolute change: a budget change reads as the budget it set.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Step** | **string** | The id of the step that made it, for example &#x60;budget&#x60;. | 
**Type** | **string** |  | 
**Status** | **string** |  | 
**Reason** | **string** | Why it was skipped or failed, such as &#x60;already_paused&#x60;, &#x60;daily_limit_reached&#x60; or &#x60;awaiting_approval&#x60;. | 
**Previous** | [**AutomationChangedValue**](AutomationChangedValue.md) |  | 
**Target** | [**AutomationChangedValue**](AutomationChangedValue.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

