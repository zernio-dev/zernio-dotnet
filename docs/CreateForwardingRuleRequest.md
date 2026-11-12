# Zernio.Model.CreateForwardingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**AccountId** | **string** | Connected ads account ID that owns the destination. | 
**DestinationId** | **string** | The platform destination: a pixel, a conversion action, a conversion rule, or a GA4 web stream measurement id (&#x60;G-…&#x60;). | 
**EventNames** | **List&lt;string&gt;** |  | [optional] 
**Sources** | **List&lt;CreateForwardingRuleRequest.SourcesEnum&gt;** | Forward only events from these sources, such as only &#x60;web&#x60; for a tracked website. Leave it out to forward events from every source. | [optional] 
**ApiSecret** | **string** | Google Analytics destinations only, and required for them: the data stream&#39;s Measurement Protocol API secret, from GA4 Admin › Data streams › Measurement Protocol API secrets. Checked with one hit to Google&#39;s validation server (which cannot confirm the secret itself), stored encrypted and never returned. Change it later with &#x60;PATCH /v1/events/forwarding-rules/{ruleId}&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

