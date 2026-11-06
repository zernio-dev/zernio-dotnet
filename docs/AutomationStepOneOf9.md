# Zernio.Model.AutomationStepOneOf9
Moves daily budget from the matched objects ranked worst by `metric` over `window` to those ranked best. The total stays the same.  Send `by` (a percent of each giver's budget) or `amount` (in all, split evenly), not both. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Type** | **string** |  | 
**Metric** | **string** | A condition metric or &#x60;result:&lt;key&gt;&#x60;, not a calendar metric. | 
**Window** | **string** | A condition window. | 
**Best** | **string** | Which end is best. Defaults to lowest for &#x60;cpa&#x60;, &#x60;cpc&#x60;, &#x60;cpm&#x60;, &#x60;frequency&#x60; and cost results, highest otherwise. | [optional] 
**From** | **int** | How many objects give budget. | 
**To** | **int** | How many objects receive it. | 
**By** | **string** | From 1% to 90%. | [optional] 
**Amount** | **decimal** |  | [optional] 
**Min** | **decimal** | A giver&#39;s budget never goes below this. | [optional] 
**Max** | **decimal** | A receiver&#39;s budget never goes above this. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

