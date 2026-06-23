# Zernio.Model.ListInstagramStories200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Instagram media ID of the story. | 
**MediaType** | **string** | IMAGE / VIDEO / CAROUSEL_ALBUM | [optional] 
**MediaProductType** | **string** | Always &#39;STORY&#39; for this endpoint. | [optional] 
**MediaUrl** | **string** | Direct media URL. Null if Meta flagged the story for copyright. URL expires when the story expires. | [optional] 
**Permalink** | **string** | Public Instagram permalink to the story (only viewable while live). | [optional] 
**ThumbnailUrl** | **string** | Thumbnail URL for video stories. | [optional] 
**Timestamp** | **DateTime?** | When the story was posted. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

