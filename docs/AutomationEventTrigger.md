# Zernio.Model.AutomationEventTrigger
Starts the automation when something happens in Zernio, in one profile. `GET /v1/automations/catalog` lists every event with its facts. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | The Zernio event that starts it. | 
**ProfileId** | **string** | The profile whose events start it, from &#x60;GET /v1/profiles&#x60;. | 
**AccountIds** | **List&lt;string&gt;** | Only events of these accounts. Leave out for every account of the profile. | [optional] 
**Filter** | [**AutomationFactCondition**](AutomationFactCondition.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

