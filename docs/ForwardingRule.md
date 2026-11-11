# Zernio.Model.ForwardingRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Rule ID, used to delete it. | [optional] 
**ProfileId** | **string** |  | [optional] 
**AccountId** | **string** |  | [optional] 
**DestinationId** | **string** | Platform destination (pixel, conversion action, rule, ...). | [optional] 
**EventNames** | **List&lt;string&gt;** | Event names forwarded to this destination; null forwards every event. | [optional] 
**Sources** | **List&lt;ForwardingRule.SourcesEnum&gt;** | Event sources forwarded to this destination; null forwards events from every source. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

