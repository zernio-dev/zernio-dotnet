# Zernio.Model.SendEvents200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**DestinationId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**EventsSent** | **int** | Events the platform accepted. | [optional] 
**EventsFailed** | **int** |  | [optional] 
**Failures** | [**List&lt;SendEvents200ResponseDestinationsInnerFailuresInner&gt;**](SendEvents200ResponseDestinationsInnerFailuresInner.md) |  | [optional] 
**Error** | **string** | Set when the destination could not be reached at all (account disconnected, unsupported platform, platform error). | [optional] 
**Retrying** | **bool** | The destination failed for now (platform error, timeout, rate limit) and the send is queued for retries; its outcome shows on GET /v1/events/{eventId}. | [optional] 
**TraceId** | **string** | The platform trace ID of the send (Meta &#x60;fbtrace_id&#x60;, Google &#x60;requestId&#x60;, TikTok &#x60;request_id&#x60;), to quote to the platform support. Absent when the platform returns none. | [optional] 
**PlatformMessages** | **List&lt;string&gt;** | Meta&#39;s &#x60;messages&#x60; (warnings about the events it accepted), each distinct one once, at most 20. Absent when the platform sent none. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

