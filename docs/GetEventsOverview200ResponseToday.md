# Zernio.Model.GetEventsOverview200ResponseToday

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Conversions** | **int** | Stored events that occurred today, retracted ones excluded. | [optional] 
**Value** | **decimal** | Value of those events in &#x60;currency&#x60;. Events in other currencies are left out. | [optional] 
**Currency** | **string** | The currency most of today&#39;s valued events use; &#x60;null&#x60; when none carried a value. | [optional] 
**Sent** | **int** | Event sends to a destination today, one per event and destination. | [optional] 
**Accepted** | **int** | Those whose latest send the platform accepted. | [optional] 
**Matched** | **int** | Today&#39;s events matched to an ad campaign. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

