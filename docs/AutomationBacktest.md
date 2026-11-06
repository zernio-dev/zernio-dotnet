# Zernio.Model.AutomationBacktest
What the automation would have done on each past day, replayed on stored daily metrics. Nothing is changed.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**From** | **DateOnly** | The first day replayed, in the ad account timezone. | 
**To** | **DateOnly** | The last day replayed, yesterday in the ad account timezone. | 
**Timezone** | **string** |  | 
**TimezoneAssumed** | **bool** | True when the ad account timezone is unknown and UTC was used. | 
**Currency** | **string** |  | 
**Totals** | [**AutomationBacktestTotals**](AutomationBacktestTotals.md) |  | 
**Days** | [**List&lt;AutomationBacktestDay&gt;**](AutomationBacktestDay.md) |  | 
**Notes** | [**List&lt;AutomationBacktestNotesInner&gt;**](AutomationBacktestNotesInner.md) | What this replay could not know, for example that budgets have no history. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

