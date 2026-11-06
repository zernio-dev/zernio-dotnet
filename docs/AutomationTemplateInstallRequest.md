# Zernio.Model.AutomationTemplateInstallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Inputs** | **Dictionary&lt;string, Object&gt;** | A value for each input, by its &#x60;key&#x60;. Required inputs without a default must be sent. | [optional] 
**Targets** | [**List&lt;AutomationTemplateInstallRequestTargetsInner&gt;**](AutomationTemplateInstallRequestTargetsInner.md) | Install several times in one call, for example on many ad accounts. Each target is its own install, all or nothing, and its &#x60;inputs&#x60; win over the shared &#x60;inputs&#x60;. A failed target leaves the others in place. | [optional] 
**Status** | **string** | The status of every automation created. | [optional] [default to StatusEnum.Paused]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

