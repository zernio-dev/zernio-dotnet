# Zernio.Model.AdRuleObjectEvaluationConditionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Metric** | **string** |  | 
**Window** | **string** | Days in the ad account&#39;s own timezone. &#x60;last_7d&#x60; is the 7 full days before today; only &#x60;today&#x60; reads the day in progress. | 
**Op** | **string** |  | 
**Value** | **decimal** |  | 
**Actual** | **decimal?** | The object&#39;s value over the window. Null when it cannot be computed. | 
**Met** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

