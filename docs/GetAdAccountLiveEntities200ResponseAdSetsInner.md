# Zernio.Model.GetAdAccountLiveEntities200ResponseAdSetsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformAdSetId** | **string** |  | [optional] 
**AdSetName** | **string** |  | [optional] 
**PlatformCampaignId** | **string** |  | [optional] 
**PlatformAdSetStatus** | **string** | Meta &#x60;effective_status&#x60;, for example ACTIVE, PAUSED, CAMPAIGN_PAUSED. | [optional] 
**ConfiguredStatus** | **string** | Meta &#x60;status&#x60;: the ad set&#39;s own switch. | [optional] 
**Status** | **string** | Zernio&#39;s normalized status, derived from &#x60;platformAdSetStatus&#x60;. | [optional] 
**Budget** | [**GetAdAccountLiveEntities200ResponseAdSetsInnerBudget**](GetAdAccountLiveEntities200ResponseAdSetsInnerBudget.md) |  | [optional] 
**DailyBudget** | **decimal?** | Meta &#x60;daily_budget&#x60; in whole units of &#x60;currency&#x60;. | [optional] 
**LifetimeBudget** | **decimal?** | Meta &#x60;lifetime_budget&#x60; in whole units of &#x60;currency&#x60;. | [optional] 
**BudgetRemaining** | **decimal?** | Meta &#x60;budget_remaining&#x60; in whole units of &#x60;currency&#x60;. Null when the ad set has no budget of its own. | [optional] 
**BidStrategy** | **string** | Meta &#x60;bid_strategy&#x60;. | [optional] 
**BidAmount** | **decimal?** | Meta &#x60;bid_amount&#x60; (bid cap or cost target) in whole units of &#x60;currency&#x60;. Null when the strategy has none. | [optional] 
**OptimizationGoal** | **string** | Meta &#x60;optimization_goal&#x60;. | [optional] 
**BillingEvent** | **string** | Meta &#x60;billing_event&#x60;. | [optional] 
**PromotedObject** | **Dictionary&lt;string, Object&gt;** | Meta &#x60;promoted_object&#x60; verbatim (snake_case). | [optional] 
**Targeting** | **Dictionary&lt;string, Object&gt;** | Meta &#x60;targeting&#x60; verbatim (snake_case), as Meta returns it now. | [optional] 
**Schedule** | [**GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule**](GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

