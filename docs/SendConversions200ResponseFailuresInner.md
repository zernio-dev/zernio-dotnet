# Zernio.Model.SendConversions200ResponseFailuresInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventIndex** | **int** | Index into the submitted events array. | [optional] 
**EventId** | **string** | Echoes back the eventId of the failed event. | [optional] 
**Message** | **string** |  | [optional] 
**Code** | [**SendConversions200ResponseFailuresInnerCode**](SendConversions200ResponseFailuresInnerCode.md) |  | [optional] 
**Field** | **string** | Google Ads and Campaign Manager 360 only: the event field Google refused (&#x60;event_timestamp&#x60;, &#x60;currency&#x60;...), without the &#x60;events.events[N].&#x60; prefix. Absent when Google named the event but no field. | [optional] 
**Scope** | **string** | Google Ads and Campaign Manager 360 only, when Google refused the request. Absent for other platforms.  - &#x60;event&#x60;: Google named this event, and &#x60;message&#x60; is its own violation. - &#x60;batch&#x60;: the refusal is about the whole request (destination, account, an outage) and is copied to every event of it. - &#x60;batch_rejected&#x60;: Google did not name this event, but its resend without the named events failed too. &#x60;message&#x60; is that resend&#39;s error. | [optional] 
**PlatformError** | **Dictionary&lt;string, Object&gt;** | Meta only. Meta&#39;s own error for the rejected chunk, with credentials redacted: &#x60;message&#x60;, &#x60;type&#x60;, &#x60;code&#x60;, &#x60;error_subcode&#x60;, &#x60;error_user_title&#x60;, &#x60;error_user_msg&#x60; and &#x60;fbtrace_id&#x60; when Meta sends them. &#x60;message&#x60; above already ends with &#x60;error_user_msg&#x60;. Absent when Meta returned no error body.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

