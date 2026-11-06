# Zernio.Model.AutomationBacktestTotals

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Actions** | **int** | Actions it would have taken. Skipped ones are not counted. | 
**Pauses** | **int** |  | 
**Activations** | **int** |  | 
**BudgetRaised** | **int** | Budget changes that raised a budget. | 
**BudgetLowered** | **int** | Budget changes that lowered a budget. | 
**BudgetChange** | **decimal** | The net budget change across every budget action, in &#x60;currency&#x60;. | 
**Notifications** | **int** |  | 
**Skipped** | **int** | Actions planned but skipped. | 
**Subjects** | **int** | Distinct objects it would have acted on. | 
**HeldBack** | **int** | Matches left alone by the cooldown or a cap, summed over the days. | 
**DaysWithActions** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

