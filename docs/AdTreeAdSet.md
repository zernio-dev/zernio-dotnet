# Zernio.Model.AdTreeAdSet
Ad set (or ad group/line item depending on platform) with rolled-up metrics and child ads

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformAdSetId** | **string** |  | [optional] 
**AdSetName** | **string** |  | [optional] 
**Status** | **AdStatus** | Derived from child ad statuses | [optional] 
**AdCount** | **int** |  | [optional] 
**Budget** | [**AdTreeAdSetBudget**](AdTreeAdSetBudget.md) |  | [optional] 
**AdSetBudget** | [**AdTreeAdSetAdSetBudget**](AdTreeAdSetAdSetBudget.md) |  | [optional] 
**Metrics** | [**AdMetrics**](AdMetrics.md) |  | [optional] 
**OptimizationGoal** | **string** | What the delivery system optimizes for. Meta ad set optimization goal (e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION), or on LinkedIn the campaign&#39;s effective optimizationTargetType (NONE means manual bidding). See the &#x60;optimizationGoal&#x60; field on &#x60;Ad&#x60; for the full value spaces. | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal?** | Bid amount in whole currency units. On Meta/TikTok populated when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP; on LinkedIn it is the campaign&#39;s effective unitCost and pairs with &#x60;costType&#x60;, where 0 is a real, delivery-stopping value. | [optional] 
**RoasAverageFloor** | **decimal?** | Minimum ROAS as a decimal multiplier (2.0 &#x3D; 2.0x). Populated when bidStrategy is LOWEST_COST_WITH_MIN_ROAS. | [optional] 
**CostType** | **string** | LinkedIn only. Effective cost model (billing event) of the LinkedIn campaign backing this ad set: CPM, CPC or CPV. Null for non-LinkedIn ad sets. | [optional] 
**ServingStatuses** | **List&lt;string&gt;** | LinkedIn only. Why the LinkedIn campaign backing this ad set is (or is not) delivering. A LinkedIn Campaign maps to this ad-set node, so this is the level where LinkedIn&#39;s holds actually apply. Empty means no serving data, [\&quot;RUNNABLE\&quot;] means eligible to serve, anything else is a hold. See the &#x60;servingStatuses&#x60; field on &#x60;Ad&#x60; for the known values. | [optional] 
**PromotedObject** | [**AdTreeAdSetPromotedObject**](AdTreeAdSetPromotedObject.md) |  | [optional] 
**Ads** | [**List&lt;Ad&gt;**](Ad.md) | Individual ads within this ad set (capped at 100). Returns a subset of Ad fields from the aggregation (core fields like _id, name, platform, status, budget, metrics, creative, goal are included; targeting and schedule may be absent). When &#x60;timeIncrement&#x3D;1&amp;dailyLevel&#x3D;ad&#x60;, each entry also carries a &#x60;daily[]&#x60; array of &#x60;AdDailyMetrics&#x60;. | [optional] 
**Daily** | [**List&lt;AdDailyMetrics&gt;**](AdDailyMetrics.md) | Per-day metric series for this ad set. Present only when &#x60;GET /v1/ads/tree&#x60; is called with &#x60;timeIncrement&#x3D;1&#x60; and &#x60;dailyLevel&#x60; is &#x60;adset&#x60; or &#x60;ad&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

