# Zernio.Model.SendInboxMessage429Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Error** | **string** |  | 
**Type** | **string** | Error class for programmatic handling. | 
**Code** | **string** |  | 
**Param** | **string** | The request field that caused the error, when applicable. | [optional] 
**DocUrl** | **string** | Documentation page for resolving the error, when one applies. | [optional] 
**Platform** | **string** |  | 
**PlatformError** | [**WhatsAppTemplateLookupErrorPlatformError**](WhatsAppTemplateLookupErrorPlatformError.md) |  | [optional] 
**Provider** | **string** | Email API: the mailbox provider the error came from (&#x60;google&#x60;, &#x60;microsoft&#x60;). | [optional] 
**ProviderError** | [**ErrorResponseProviderError**](ErrorResponseProviderError.md) |  | [optional] 
**Retryable** | **bool** | Email API: whether the same request can succeed if retried (with the same &#x60;Idempotency-Key&#x60; for sends). | [optional] 
**RequestId** | **string** | Email API: the request id, also in the &#x60;X-Request-Id&#x60; header. Quote it when you contact support. | [optional] 
**DocsUrl** | **string** | Email API: where this &#x60;code&#x60; is documented. | [optional] 
**Details** | [**WhatsAppTemplateLookupErrorDetails**](WhatsAppTemplateLookupErrorDetails.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

