# Zernio.Model.InstagramHashtagMedia

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Instagram media ID of a public post carrying the hashtag. | 
**Caption** | **string** |  | 
**MediaType** | **string** | IMAGE, VIDEO or CAROUSEL_ALBUM. | 
**MediaProductType** | **string** | Always null. Meta does not serve it on hashtag media. | 
**MediaUrl** | **string** | Temporary CDN URL. Meta omits it for videos with copyrighted audio and for carousel albums. | 
**ThumbnailUrl** | **string** | Always null. Meta does not serve it on hashtag media. | 
**Permalink** | **string** | Public Instagram URL of the post. | 
**Timestamp** | **string** | Publication time as Meta returns it (ISO 8601). | 
**LikeCount** | **int?** | Null when the owner hides like counts. | 
**CommentsCount** | **int?** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

