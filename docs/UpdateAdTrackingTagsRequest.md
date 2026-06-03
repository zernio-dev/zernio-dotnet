# Zernio.Model.UpdateAdTrackingTagsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UrlTags** | [**List&lt;UpdateAdTrackingTagsRequestUrlTagsInner&gt;**](UpdateAdTrackingTagsRequestUrlTagsInner.md) | Meta only. Click-URL params appended to a freshly-rebuilt creative. | [optional] 
**Creative** | [**UpdateAdTrackingTagsRequestCreative**](UpdateAdTrackingTagsRequestCreative.md) |  | [optional] 
**TrackingUrlTemplate** | **string** | Google only. Full tracking template (must contain {lpurl}). | [optional] 
**FinalUrlSuffix** | **string** | Google only. Parse-only key&#x3D;value params. | [optional] 
**DynamicValueParameters** | **Dictionary&lt;string, string&gt;** | LinkedIn only. key -&gt; dynamic value enum (CAMPAIGN_ID, CAMPAIGN_NAME, CREATIVE_ID, ...). | [optional] 
**CustomValueParameters** | **Dictionary&lt;string, string&gt;** | LinkedIn only. key -&gt; static value. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

