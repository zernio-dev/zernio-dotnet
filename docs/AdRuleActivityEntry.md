# Zernio.Model.AdRuleActivityEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable ID of this entry. | 
**RanAt** | **DateTime** |  | 
**RuleId** | **string** |  | 
**RuleName** | **string** | The rule&#39;s name when it acted. | 
**Platform** | **string** |  | 
**AccountId** | **string** | The ads connection the rule runs on. | 
**AdAccountId** | **string** |  | 
**Level** | **string** |  | 
**ObjectId** | **string** | Platform ID of the campaign or ad set. | 
**ObjectName** | **string** | Its name when the rule acted. | 
**Type** | **string** |  | 
**Status** | **string** |  | 
**Reason** | **string** | Why it was skipped or failed, for example &#x60;already_paused&#x60;. | 
**PreviousDailyBudget** | **decimal?** |  | 
**NewDailyBudget** | **decimal?** |  | 
**PreviousName** | **string** | The name before an &#x60;edit_name&#x60;. | 
**NewName** | **string** | The name an applied &#x60;edit_name&#x60; set. | 
**PreviousBidAmount** | **decimal?** | The bid cap or cost cap before an &#x60;adjust_bid&#x60;. | 
**NewBidAmount** | **decimal?** | The cap an applied &#x60;adjust_bid&#x60; set. | 
**TargetMetric** | **string** | Which target an &#x60;adjust_target&#x60; moved. | 
**PreviousTarget** | **decimal?** | The target CPA or target ROAS before an &#x60;adjust_target&#x60;. | 
**NewTarget** | **decimal?** | The target an applied &#x60;adjust_target&#x60; set. | 
**Currency** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

