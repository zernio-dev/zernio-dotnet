# Zernio.Model.CalendarAvailabilityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Participants** | [**List&lt;CalendarAvailabilityRequestParticipantsInner&gt;**](CalendarAvailabilityRequestParticipantsInner.md) |  | 
**From** | **DateTime** |  | 
**To** | **DateTime** |  | 
**DurationMinutes** | **int** |  | 
**IntervalMinutes** | **int** |  | [optional] [default to 30]
**RoundTo** | **int** | Rounds the first candidate slot up to this many minutes. | [optional] 
**Buffer** | [**CalendarAvailabilityRequestBuffer**](CalendarAvailabilityRequestBuffer.md) |  | [optional] 
**DefaultOpenHours** | [**List&lt;OpenHoursInner&gt;**](OpenHoursInner.md) |  | [optional] 
**Method** | **string** |  | [optional] [default to MethodEnum.Collective]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

