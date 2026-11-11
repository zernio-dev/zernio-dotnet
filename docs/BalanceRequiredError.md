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
**Provider** | **string** | Email API: the mailbox provider the error came from (&#x60;google&#x60;, &#x60;microsoft&#x60;). | [optional] 
**ProviderError** | [**ErrorResponseProviderError**](ErrorResponseProviderError.md) |  | [optional] 
**Retryable** | **bool** | Email API: whether the same request can succeed if retried (with the same &#x60;Idempotency-Key&#x60; for sends). | [optional] 
**RequestId** | **string** | Email API: the request id, also in the &#x60;X-Request-Id&#x60; header. Quote it when you contact support. | [optional] 
**DocsUrl** | **string** | Email API: where this &#x60;code&#x60; is documented. | [optional] 
**Details** | [**ErrorResponseDetails**](ErrorResponseDetails.md) |  | [optional] 
**FundingUrl** | **string** | Dashboard link to Billing that opens the Add funds drawer (the add-card drawer first when there is no card). Send the user there, then retry. | 
**RequiredCents** | **int** | Only when an item debited later (a phone number&#39;s first month, all numbers of the order) is refused: what the balance must hold, in cents. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

