# Zernio.Model.EventAutomationDefinitionStepsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**To** | [**List&lt;AutomationNotifyStepToInner&gt;**](AutomationNotifyStepToInner.md) | Up to 5 in an ad rule. | [optional] 
**Text** | **string** |  | 
**WorkflowId** | **string** |  | 
**SequenceId** | **string** |  | 
**Url** | **string** |  | 
**Method** | **string** |  | [optional] [default to MethodEnum.POST]
**Headers** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**Body** | **string** | May read &#x60;{{event.&lt;fact&gt;}}&#x60;. | [optional] 
**Action** | **string** |  | 
**Tag** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

