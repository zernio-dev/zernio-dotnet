# Zernio.Model.CreateStandaloneAdRequestCreativesInner
Each creative must supply EXACTLY ONE of `imageUrl` (image creative) or `video` (video creative).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Exact name for this ad. Falls back to &#x60;&lt;name&gt; #N&#x60; (N &#x3D; 1-based position). | [optional] 
**Headline** | **string** |  | 
**Body** | **string** |  | 
**Description** | **string** | Link description for this ad (link_data.description; video creatives: video_data.link_description). Falls back to the top-level &#x60;description&#x60;; when both are omitted Meta scrapes the destination URL&#39;s OG description. | [optional] 
**ImageUrl** | **string** | Image creative. Mutually exclusive with &#x60;video&#x60;. | [optional] 
**Video** | [**CreateStandaloneAdRequestCreativesInnerVideo**](CreateStandaloneAdRequestCreativesInnerVideo.md) |  | [optional] 
**LinkUrl** | **string** |  | 
**CallToAction** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

