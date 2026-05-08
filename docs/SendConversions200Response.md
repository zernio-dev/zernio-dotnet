# Zernio.Model.SendConversions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**EventsReceived** | **int** | Events accepted by the platform. | [optional] 
**EventsFailed** | **int** | Events rejected (see failures). | [optional] 
**Failures** | [**List&lt;SendConversions200ResponseFailuresInner&gt;**](SendConversions200ResponseFailuresInner.md) |  | [optional] 
**TraceId** | **string** | Platform trace ID for debugging. fbtrace_id for Meta, requestId for Google. Absent for LinkedIn (LinkedIn&#39;s conversionEvents endpoint does not surface a trace ID).  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

