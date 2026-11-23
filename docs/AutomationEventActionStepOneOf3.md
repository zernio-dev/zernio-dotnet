# Zernio.Model.AutomationEventActionStepOneOf3
Calls an http or https URL. Without `body`, a POST sends the event's type, id and facts as JSON. Fits every event.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**Url** | **string** |  | 
**Method** | **string** |  | [optional] [default to MethodEnum.POST]
**Headers** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**Body** | **string** | May read &#x60;{{event.&lt;fact&gt;}}&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

