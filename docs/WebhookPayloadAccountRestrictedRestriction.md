# Zernio.Model.WebhookPayloadAccountRestrictedRestriction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Reason** | **string** | &#x60;suspended&#x60;: banned or suspended by the platform. &#x60;restricted&#x60;: locked, restricted or blocked from posting. &#x60;verification_required&#x60;: the platform asks for an identity or security check. &#x60;auth_expired&#x60;: the login stopped working; reconnect. | 
**Message** | **string** | The error the last failed post carries. | 
**PlatformError** | [**WebhookPayloadAccountRestrictedRestrictionPlatformError**](WebhookPayloadAccountRestrictedRestrictionPlatformError.md) |  | 
**ConsecutiveFailures** | **int** | Identical failures in a row that restricted the account. | 
**Since** | **DateTime** |  | 
**PostId** | **string** | The post whose failure restricted the account. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

