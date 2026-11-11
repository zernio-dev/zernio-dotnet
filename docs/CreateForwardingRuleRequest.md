# Zernio.Model.CreateForwardingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**AccountId** | **string** | Connected ads account ID that owns the destination. | 
**DestinationId** | **string** | The platform destination: a pixel, a conversion action or a conversion rule. | 
**EventNames** | **List&lt;string&gt;** |  | [optional] 
**Sources** | **List&lt;CreateForwardingRuleRequest.SourcesEnum&gt;** | Forward only events from these sources, such as only &#x60;web&#x60; for a tracked website. Leave it out to forward events from every source. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

