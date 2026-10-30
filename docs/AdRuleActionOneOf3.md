# Zernio.Model.AdRuleActionOneOf3

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | Change the daily budget. Not on ad-level rules (an ad has no budget), and on Google it needs a campaign-level rule (ad groups have no budget of their own). | 
**Direction** | **string** |  | 
**Percent** | **int** | Change in percent: up to 100 for an increase, up to 90 for a decrease. | 
**Limit** | **decimal** | The budget never goes above this on an increase, or below it on a decrease, in the ad account currency. | 
**MaxChangesPerDay** | **int** | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with &#x60;daily_limit_reached&#x60; and tried again later. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

