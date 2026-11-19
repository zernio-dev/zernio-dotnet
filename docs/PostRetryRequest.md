# Zernio.Model.PostRetryRequest
Optional. Omit the body to retry every failed or pending platform of the post.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platforms** | [**List&lt;PostRetryRequestPlatformsInner&gt;**](PostRetryRequestPlatformsInner.md) | Retry only these platforms. Platforms not listed are left as they are, so a platform that already published is never posted twice. Each entry matches the post platforms with that &#x60;platform&#x60; and, when given, that &#x60;accountId&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

