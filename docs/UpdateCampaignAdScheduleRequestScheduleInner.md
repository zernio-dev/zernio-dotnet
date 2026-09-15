# Zernio.Model.UpdateCampaignAdScheduleRequestScheduleInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DayOfWeek** | **string** |  | 
**StartHour** | **int** |  | 
**StartMinute** | **int** | Quarter-hours only. | [optional] [default to StartMinuteEnum.NUMBER_0]
**EndHour** | **int** | 24 means midnight at the end of the day. | 
**EndMinute** | **int** | Quarter-hours only. Must be 0 when endHour is 24. | [optional] [default to EndMinuteEnum.NUMBER_0]
**BidModifier** | **decimal?** | Bid adjustment for this window. Null runs it at the campaign bid. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

