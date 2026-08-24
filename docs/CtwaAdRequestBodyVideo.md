# Zernio.Model.CtwaAdRequestBodyVideo
Video creative for single-creative shape. Mutually exclusive with `imageUrl` and with `creatives[]`. Required on the single-creative shape if `imageUrl` is not supplied. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Url** | **string** | Public URL of the video to upload. Provide either &#x60;url&#x60; or &#x60;id&#x60;. | [optional] 
**Id** | **string** | Reuse a video already uploaded to this ad account (list them with GET /v1/ads/videos) instead of re-uploading. Wins over &#x60;url&#x60;. Provide either &#x60;url&#x60; or &#x60;id&#x60;. | [optional] 
**ThumbnailUrl** | **string** | OPTIONAL: when omitted, the poster is auto-generated from Meta&#39;s own preferred video thumbnail. When Meta produces no candidate the request fails with a 502 platform_error (reason: video_thumbnail_unavailable) — retry, or supply this field to control the poster frame exactly.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

