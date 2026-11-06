# Zernio.Model.AutomationFactCondition
Narrows by the facts of the event or post, such as `platform` or `likes`: one comparison, or a group where `all` must hold or `any` is enough. Groups nest.  A leaf whose `field` is not a fact of the event or post is refused. Text compares ignoring case. A number or date that does not parse never matches. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Field** | **string** | A fact name from the catalog. | 
**Op** | **string** |  | 
**Value** | [**AutomationFactConditionOneOfValue**](AutomationFactConditionOneOfValue.md) |  | 
**All** | [**List&lt;AutomationFactCondition&gt;**](AutomationFactCondition.md) |  | 
**Any** | [**List&lt;AutomationFactCondition&gt;**](AutomationFactCondition.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

