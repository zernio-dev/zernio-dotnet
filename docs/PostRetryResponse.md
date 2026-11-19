# Zernio.Model.PostRetryResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** |  | [optional] 
**Error** | **string** | Present on a 207 only: summary of why the retry did not fully succeed. | [optional] 
**PlatformResults** | [**List&lt;PostRetryPlatformResult&gt;**](PostRetryPlatformResult.md) | One entry per platform of the post, in &#x60;post.platforms[]&#x60; order. | [optional] 
**Post** | [**Post**](Post.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

