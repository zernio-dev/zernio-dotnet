# Zernio.Model.BalanceRequiredError
The error envelope of a $0 balance refusal (402 `insufficient_balance` or `usage_limit_reached`), plus where to fund the balance.

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
**Details** | [**ErrorResponseDetails**](ErrorResponseDetails.md) |  | [optional] 
**FundingUrl** | **string** | Dashboard link to Billing that opens the top-up drawer (the add-card drawer first when there is no card). Send the user there, then retry. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

