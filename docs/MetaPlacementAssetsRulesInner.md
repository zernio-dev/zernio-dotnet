# Zernio.Model.MetaPlacementAssetsRulesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ImageUrl** | **string** | Image mode. The image to deliver for this rule&#39;s placements. | [optional] 
**VideoUrl** | **string** | Video mode. The video to deliver for this rule&#39;s placements. Each rule needs this or &#x60;videoId&#x60;. | [optional] 
**VideoId** | **string** | Video mode. ID of a video already on the ad account, used for this rule instead of uploading &#x60;videoUrl&#x60;. Wins over &#x60;videoUrl&#x60;. A video still processing after 30 seconds returns 409. | [optional] 
**ThumbnailUrl** | **string** | Video mode (optional). Poster image for this rule&#39;s video; auto-generated when omitted. | [optional] 
**Headline** | **string** | One headline pinned to this rule. Omit to inherit the top-level headline. | [optional] 
**Body** | **string** | One primary text pinned to this rule. Omit to inherit the top-level body. | [optional] 
**Description** | **string** | One link description pinned to this rule. Omit to inherit the top-level description. | [optional] 
**Placements** | [**MetaPlacementAssetsRulesInnerPlacements**](MetaPlacementAssetsRulesInnerPlacements.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

