# Zernio.Model.PostRetryPlatformResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** | Platform slug, matching &#x60;post.platforms[].platform&#x60;. | 
**AccountId** | **string** | Account id of this platform. | 
**Retried** | **bool** | Whether this request retried the platform. False for a platform that had already published, or one left out of &#x60;platforms&#x60;. | 
**Status** | **string** | Status after the retry: pending, processing, published, failed, cancelled, uploading. | 
**Error** | **string** | Failure message for this platform, or null when it did not fail. | 
**ErrorCategory** | **string** | Stable failure category (for example &#x60;auth_expired&#x60;, &#x60;account_issue&#x60;, &#x60;user_content&#x60;, &#x60;platform_error&#x60;), or null. | 
**ErrorSource** | **string** | Who caused the failure (&#x60;user&#x60;, &#x60;platform&#x60; or &#x60;system&#x60;), or null. | 
**PlatformErrorCode** | **int?** | Error code returned by the platform, when it sent one. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

