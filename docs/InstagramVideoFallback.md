# Zernio.Model.InstagramVideoFallback
Meta only. Present when Meta refused an existing Instagram video as the boosted ad (code 100, subcode 1815279: upload it to Facebook first) and Zernio created the ad another way:  - `instagram_video_reuploaded`: the video was copied into the ad account, and the ad still references the original post. - `instagram_video_rehosted_copy`: the video was uploaded as a new Facebook video in a new Page post, so the ad does not show the original post's likes and comments.  Send `rehostOnInstagramVideoRejection: false` on the boost to get Meta's error instead. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | **string** |  | 
**LinkedToOriginalPost** | **bool** | True when the ad still references the original Instagram post and keeps its engagement. | 
**VideoId** | **string** | The Facebook-side ad video Zernio made.  - instagram_video_reuploaded: the copy in the ad account video library (possibly one made by an earlier boost of the same media, reused). The creative carries it as video_id, unless Meta accepted the plain post reference once the copy existed; then the copy is kept for that reference. - instagram_video_rehosted_copy: the new upload the creative uses (an unused copy made by this request is deleted). | 
**PlatformError** | [**InstagramVideoFallbackPlatformError**](InstagramVideoFallbackPlatformError.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

