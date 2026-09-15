# Zernio.Model.GetCampaignAdSchedule200ResponsePerformance
Only present when includePerformance=true.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**WindowDays** | **int?** | The trailing window used, or null when an explicit fromDate/toDate range was given. | [optional] 
**ByDayOfWeek** | [**List&lt;GetCampaignAdSchedule200ResponsePerformanceByDayOfWeekInner&gt;**](GetCampaignAdSchedule200ResponsePerformanceByDayOfWeekInner.md) | One entry per day that delivered, Monday first. | [optional] 
**ByHour** | [**List&lt;GetCampaignAdSchedule200ResponsePerformanceByHourInner&gt;**](GetCampaignAdSchedule200ResponsePerformanceByHourInner.md) | One entry per hour that delivered, 0-23 in the account time zone. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

