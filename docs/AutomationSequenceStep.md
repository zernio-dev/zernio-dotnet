# Zernio.Model.AutomationSequenceStep
Waits `after` the previous step (the first, after the enrollment), then sends `message`, or `template` on WhatsApp. Needs `message.text`, `message.attachments` or `template.name`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**After** | **string** | Whole minutes as a duration, such as &#x60;0m&#x60;, &#x60;90m&#x60; or &#x60;1d&#x60;. | 
**Message** | [**AutomationSequenceStepMessage**](AutomationSequenceStepMessage.md) |  | [optional] 
**Template** | [**AutomationSequenceStepTemplate**](AutomationSequenceStepTemplate.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

