# Zernio.Model.GetEventsOverviewDaily200ResponseDaysInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Day** | **DateOnly** |  | [optional] 
**Conversions** | **int** | Stored events that occurred that day. | [optional] 
**Sent** | **int** | Events first sent to a destination that day. | [optional] 
**Accepted** | **int** | Those the platform accepted. | [optional] 
**Value** | **decimal** | The day&#39;s value, in the period&#39;s &#x60;totals.currency&#x60;. | [optional] 
**ValueSent** | **decimal** | Of that value, the conversions a platform accepted. | [optional] 
**FromAds** | **int** | Counted events that came from an ad, as in &#x60;totals.fromAds&#x60;. | [optional] 
**Matched** | **int** | Events matched to an ad campaign. | [optional] 
**ByEvent** | **Dictionary&lt;string, int&gt;** | The day&#39;s stored events per event name. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

