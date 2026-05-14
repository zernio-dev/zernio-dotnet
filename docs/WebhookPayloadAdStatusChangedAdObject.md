# Zernio.Model.WebhookPayloadAdStatusChangedAdObject
The ad-platform object the status change applies to.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Level** | **string** | Hierarchy level the status applies to. Mirrors Meta&#39;s &#x60;level&#x60;. Creative-level events are not forwarded. | 
**PlatformId** | **string** | Platform-native ID of the campaign / ad set / ad. For Meta this is the bare numeric ID (e.g. &#x60;120244894077860689&#x60;).  | 
**PlatformAdAccountId** | **string** | Platform-native ad-account ID. For Meta this uses the &#x60;act_&lt;id&gt;&#x60; shape.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

