# Zernio.Model.PostPublishIncompleteResponse
Body of the 207 returned by createPost and updatePost when the post was saved but the inline publish did not fully succeed. Read `post.status` to tell the three outcomes apart.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Post** | [**Post**](Post.md) |  | [optional] 
**Message** | **string** | Human-readable summary of the publish outcome. | [optional] 
**Error** | **string** | Present when no platform published. Absent on a partial success. Informational only; the per-platform detail is in &#x60;platformResults&#x60; and in &#x60;post.platforms[]&#x60;. | [optional] 
**PlatformResults** | [**List&lt;PostPublishIncompleteResponsePlatformResultsInner&gt;**](PostPublishIncompleteResponsePlatformResultsInner.md) | Per-platform outcome of the publish attempt. Omitted when the attempt aborted before producing per-platform results (for example the post was already being processed); read &#x60;post.platforms[]&#x60; in that case. | [optional] 
**Warnings** | **List&lt;string&gt;** | Advisory notices about the post that was still created. Absent when there are none. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

