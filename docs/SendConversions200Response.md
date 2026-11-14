# Zernio.Model.SendConversions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**EventsReceived** | **int** | Events accepted by the platform. | [optional] 
**EventsFailed** | **int** | Events rejected (see failures). | [optional] 
**Failures** | [**List&lt;SendConversions200ResponseFailuresInner&gt;**](SendConversions200ResponseFailuresInner.md) |  | [optional] 
**TraceId** | **string** | Platform trace ID for debugging. fbtrace_id for Meta, requestId for Google, request_id for TikTok. Absent for LinkedIn (LinkedIn&#39;s conversionEvents endpoint does not surface a trace ID), OpenAI Ads and Reddit (no trace ID surfaced).  | [optional] 
**PlatformMessages** | **List&lt;string&gt;** | Meta only. Meta&#39;s &#x60;messages&#x60; (warnings about the events it accepted), each distinct one once, at most 20. Absent when Meta sent none. | [optional] 
**TestCode** | **string** | The test code sent to the platform, as received (from &#x60;testCode&#x60; or &#x60;test_event_code&#x60;). &#x60;null&#x60; when the request carried none, so the events were sent as production events. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

