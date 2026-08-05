# Zernio.Model.ValueRuleSet
A named set of bid-adjustment rules on an ad account. Attach it to an ad set with `valueRuleSetId`. Limits: 6 sets per ad account, 10 rules per set, 4 criteria per rule. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform value rule set id. | 
**Name** | **string** |  | 
**Rules** | [**List&lt;ValueRule&gt;**](ValueRule.md) | Evaluated in order; the first matching rule wins. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

