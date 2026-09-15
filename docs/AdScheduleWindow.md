# Zernio.Model.AdScheduleWindow
One ad schedule window as Google stores it. Half-open: it is exclusive of the end minute, so 09:00-12:00 and 12:00-17:00 are adjacent, not overlapping.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CriterionId** | **string** | Google campaign criterion id. Changes whenever the window is rewritten, because Google cannot edit a schedule in place. | [optional] 
**ResourceName** | **string** |  | [optional] 
**DayOfWeek** | **string** |  | [optional] 
**StartHour** | **int** |  | [optional] 
**StartMinute** | **int** |  | [optional] 
**EndHour** | **int** | 24 means midnight at the end of the day. | [optional] 
**EndMinute** | **int** |  | [optional] 
**BidModifier** | **decimal?** | Bid adjustment for this window, 0.1-10.0. Null when the window runs at the campaign bid. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

