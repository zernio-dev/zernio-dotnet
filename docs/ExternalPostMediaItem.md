# Zernio.Model.ExternalPostMediaItem
A media item on a native (external/synced) post, as carried by post.external.* webhook payloads. Distinct from the richer MediaItem used for Zernio-authored posts: external items are always already-published (url required) and limited to image or video. Kept as a separate schema so the generated SDK model does not collide with MediaItem. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Url** | **string** |  | 
**Thumbnail** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

