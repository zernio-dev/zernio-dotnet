# Zernio.Model.AdRuleObjectEvaluationConditionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Metric** | **string** | &#x60;ctr&#x60; is a percentage. &#x60;spend&#x60;, &#x60;cpc&#x60;, &#x60;cpm&#x60; and &#x60;cpa&#x60; are in the ad account currency. | 
**Window** | **string** | Days in the ad account&#39;s own timezone. &#x60;last_7d&#x60; includes today. | 
**Op** | **string** |  | 
**Value** | **decimal** |  | 
**Actual** | **decimal?** | The object&#39;s value over the window. Null when it cannot be computed. | 
**Met** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

