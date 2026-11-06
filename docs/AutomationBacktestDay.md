# Zernio.Model.AutomationBacktestDay

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **DateOnly** |  | 
**Checks** | **int** | Checks the schedule would have run that day. 0 on a day it skips. | 
**Evaluated** | **int** | The most objects any of the day&#39;s checks judged. | 
**Matched** | **int** | The most objects any of the day&#39;s checks matched. | 
**HeldBack** | **int** | Matches left alone all day by the cooldown or a cap. | 
**Actions** | [**List&lt;AutomationBacktestDayActionsInner&gt;**](AutomationBacktestDayActionsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

