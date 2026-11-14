# Zernio.Model.SendWhatsAppConversion200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**EventsReceived** | **int** | Events accepted by Meta. | [optional] 
**EventsFailed** | **int** | Events rejected by Meta (see failures). | [optional] 
**Failures** | [**List&lt;SendWhatsAppConversion200ResponseFailuresInner&gt;**](SendWhatsAppConversion200ResponseFailuresInner.md) | Per-event failure detail. Empty when all events were accepted.  | [optional] 
**TraceId** | **string** | Meta &#x60;fbtrace_id&#x60; for debugging. Surface in support tickets.  | [optional] 
**PlatformMessages** | **List&lt;string&gt;** | Meta&#39;s &#x60;messages&#x60; (warnings about the events it accepted), each distinct one once, at most 20. Absent when Meta sent none. | [optional] 
**TestCode** | **string** | The test code sent to Meta, or &#x60;null&#x60; when the request carried none. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

