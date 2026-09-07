# Zernio.Model.CreateTrackingTagRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** | Meta ad account id, e.g. &#x60;act_123456789&#x60;. Required by this endpoint but ignored for OpenAI Ads. | 
**Name** | **string** |  | 
**DefaultEventType** | **string** | OpenAI Ads only (ignored by Meta). When set, also provisions a standard conversion event setting wired to the new pixel, so &#x60;goal: conversions&#x60; ad creates on &#x60;POST /v1/ads/create&#x60; have an event to reference immediately. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

