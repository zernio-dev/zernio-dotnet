# Zernio.Model.InstagramMentionedMedia

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Instagram media ID of the post whose caption mentions the account. | 
**Caption** | **string** |  | 
**MediaType** | **string** | IMAGE, VIDEO or CAROUSEL_ALBUM. | 
**MediaUrl** | **string** | Temporary CDN URL. Meta omits it for videos with copyrighted or licensed audio and reels whose owner disabled downloads. | 
**Timestamp** | **string** | Publication time as Meta returns it (ISO 8601). | 
**Username** | **string** | Instagram handle of the account that posted the media and mentioned yours. | 
**LikeCount** | **int?** | Null when the owner hides like counts. | 
**CommentsCount** | **int?** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

