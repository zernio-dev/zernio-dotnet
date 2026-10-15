# Zernio.Model.SendInboxMessage400ResponsePlatformError
Instagram, Facebook, WhatsApp, or TikTok. The platform's diagnostic fields for the rejected send or template lookup. WhatsApp lookup errors retain only code, message, and error_data.details. On TikTok only code, message, and request_id are set. Absent when the failure did not come from the platform.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **int** | Meta or TikTok error code | [optional] 
**Subcode** | **int** | Meta error_subcode | [optional] 
**FbtraceId** | **string** | Meta fbtrace_id, quote this in a Meta bug report | [optional] 
**Type** | **string** | Meta error type (e.g. OAuthException) | [optional] 
**Message** | **string** | TikTok error message | [optional] 
**RequestId** | **string** | TikTok request_id, quote this in a TikTok support ticket | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

