# Zernio.Model.InstagramBusinessDiscoveryMediaInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Caption** | **string** |  | 
**MediaType** | **string** | IMAGE, VIDEO or CAROUSEL_ALBUM | 
**MediaProductType** | **string** | FEED or REELS | 
**Timestamp** | **DateTime?** |  | 
**Permalink** | **string** |  | 
**LikeCount** | **int?** | Null when the owner hides like counts | 
**CommentsCount** | **int?** |  | 
**MediaUrl** | **string** | Temporary CDN URL that expires; download the file rather than storing the link. Null on videos whose audio is licensed music, use thumbnailUrl for the cover. | 
**ThumbnailUrl** | **string** | Video cover frame, VIDEO only. Temporary CDN URL. | 
**ViewCount** | **int?** | Reels only. Null on images and carousels. | 
**Children** | [**List&lt;InstagramBusinessDiscoveryMediaInnerChildrenInner&gt;**](InstagramBusinessDiscoveryMediaInnerChildrenInner.md) | Carousel slides in order. Null unless mediaType is CAROUSEL_ALBUM. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

