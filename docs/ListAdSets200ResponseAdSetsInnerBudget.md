# Zernio.Model.ListAdSets200ResponseAdSetsInnerBudget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **decimal** |  | [optional] 
**Type** | **string** |  | [optional] 
**Daily** | **decimal** | LinkedIn only. The campaign&#39;s &#x60;dailyBudget&#x60;. LinkedIn allows a daily AND a lifetime budget on the same campaign, which &#x60;amount&#x60;/&#x60;type&#x60; cannot express (daily wins there); read &#x60;daily&#x60; and &#x60;lifetime&#x60; to see both. | [optional] 
**Lifetime** | **decimal** | LinkedIn only. The campaign&#39;s &#x60;totalBudget&#x60;, readable even when a daily budget is also set. | [optional] 
**Pacing** | **string** | LinkedIn only. The campaign&#39;s &#x60;pacingStrategy&#x60;: how fast LinkedIn may spend the budget. Typically LINEAR or ACCELERATED; the list is open. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

