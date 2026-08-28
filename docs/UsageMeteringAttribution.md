# Zernio.Model.UsageMeteringAttribution
Present with `groupBy`. The window's spend split per profile or account; `sum(groups) + unattributed` equals `totals` per product.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GroupBy** | **string** |  | [optional] 
**Groups** | [**List&lt;UsageAttributionGroup&gt;**](UsageAttributionGroup.md) |  | [optional] 
**Unattributed** | [**UsageAttributionSlice**](UsageAttributionSlice.md) | Spend no profile/account can claim: credits, 10DLC fees, Verify, and usage whose record no longer resolves to an account. Zero for a restricted principal. | [optional] 
**Totals** | [**UsageAttributionSlice**](UsageAttributionSlice.md) | The window totals; for a restricted principal, the sum of the visible groups. | [optional] 
**Restricted** | **bool** | True when the caller (profile-scoped API key or member) cannot see every profile: &#x60;groups&#x60; are filtered, &#x60;totals&#x60; sum them, &#x60;unattributed&#x60; is zero, and the top-level &#x60;days&#x60; / &#x60;totals&#x60; / &#x60;lineItems&#x60; are projected onto the visible groups with &#x60;peaks&#x60;, &#x60;callUsage&#x60; and &#x60;tax&#x60; null. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

