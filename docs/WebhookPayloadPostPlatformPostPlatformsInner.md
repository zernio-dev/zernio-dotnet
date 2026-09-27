# Zernio.Model.WebhookPayloadPostPlatformPostPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**Status** | **string** |  | 
**AccountId** | **string** | SocialAccount id this platform target published through. On post.platform.* events see also the top-level &#x60;account&#x60; block. | [optional] 
**PlatformPostId** | **string** |  | [optional] 
**PublishedUrl** | **string** |  | [optional] 
**Error** | **string** |  | [optional] 
**ErrorCategory** | **string** | Present when this target failed. Same taxonomy as &#x60;platforms[].errorCategory&#x60; on GET /v1/posts. | [optional] 
**ErrorSource** | **string** | Present when this target failed. Who must act: user, platform or system (Zernio). | [optional] 
**PlatformError** | [**PostPlatformError**](PostPlatformError.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

