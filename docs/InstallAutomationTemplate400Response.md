# Zernio.Model.InstallAutomationTemplate400Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Error** | **string** | Human-readable error message. | [optional] 
**Type** | **string** | Error class for programmatic handling. | [optional] 
**Code** | **string** | Stable machine-readable error code. | [optional] 
**Param** | **string** | The request field that caused the error, when applicable. | [optional] 
**DocUrl** | **string** | Documentation page for resolving the error, when one applies. | [optional] 
**Platform** | **string** | Upstream platform (e.g. meta, google, tiktok), present when type is platform_error. | [optional] 
**PlatformError** | **Dictionary&lt;string, Object&gt;** | Raw error payload from the upstream platform, passed through verbatim so integrators can read provider-specific codes. For Meta this includes error_subcode, error_user_title, and error_user_msg.  | [optional] 
**Details** | [**AutomationProblems**](AutomationProblems.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

