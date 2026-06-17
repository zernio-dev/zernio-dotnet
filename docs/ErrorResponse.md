# Zernio.Model.ErrorResponse
Canonical error envelope. `error` is the human-readable message; `type`, `code`, `param`, `platform`, and `platformError` are top-level siblings for programmatic handling. For upstream platform failures (`type: platform_error`), `platformError` carries the provider's raw payload verbatim (for Meta: `error_subcode`, `error_user_title`, `error_user_msg`). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Error** | **string** | Human-readable error message. | [optional] 
**Type** | **string** | Error class for programmatic handling. | [optional] 
**Code** | **string** | Stable machine-readable error code. | [optional] 
**Param** | **string** | The request field that caused the error, when applicable. | [optional] 
**Platform** | **string** | Upstream platform (e.g. meta, google, tiktok) — present when type is platform_error. | [optional] 
**PlatformError** | **Dictionary&lt;string, Object&gt;** | Raw error payload from the upstream platform, passed through verbatim so integrators can read provider-specific codes. For Meta this includes error_subcode, error_user_title, and error_user_msg.  | [optional] 
**Details** | **Dictionary&lt;string, Object&gt;** | Additional structured context (e.g. field-level validation errors). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

