# Zernio.Model.InstagramTaggedMedia

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Instagram media ID of the post the account is tagged in. | 
**Caption** | **string** |  | 
**MediaType** | **string** | IMAGE, VIDEO or CAROUSEL_ALBUM. | 
**MediaProductType** | **string** | FEED or REELS. | 
**MediaUrl** | **string** | Temporary CDN URL. Meta omits it for videos with copyrighted audio, flagged videos and reels whose owner disabled downloads. | 
**ThumbnailUrl** | **string** | Cover image of a video or reel. | 
**Permalink** | **string** | Public Instagram URL of the post. | 
**Timestamp** | **string** | Publication time as Meta returns it (ISO 8601). | 
**Username** | **string** | Instagram handle of the account that posted the media and tagged yours. | 
**LikeCount** | **int?** | Null when the owner hides like counts. | 
**CommentsCount** | **int?** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

