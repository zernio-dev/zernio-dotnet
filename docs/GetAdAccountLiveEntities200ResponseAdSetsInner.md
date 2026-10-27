# Zernio.Model.GetAdAccountLiveEntities200ResponseAdSetsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformAdSetId** | **string** |  | [optional] 
**AdSetName** | **string** |  | [optional] 
**PlatformCampaignId** | **string** |  | [optional] 
**PlatformAdSetStatus** | **string** | Meta &#x60;effective_status&#x60; (ACTIVE, PAUSED, CAMPAIGN_PAUSED...) or TikTok &#x60;secondary_status&#x60; (ADGROUP_STATUS_DELIVERY_OK, ADGROUP_STATUS_AUDIT...). | [optional] 
**ConfiguredStatus** | **string** | The ad set&#39;s own switch: Meta &#x60;status&#x60;, or TikTok &#x60;operation_status&#x60; as ACTIVE / PAUSED. | [optional] 
**Status** | **string** | Zernio&#39;s normalized status, derived from &#x60;platformAdSetStatus&#x60;. | [optional] 
**Budget** | [**GetAdAccountLiveEntities200ResponseAdSetsInnerBudget**](GetAdAccountLiveEntities200ResponseAdSetsInnerBudget.md) |  | [optional] 
**DailyBudget** | **decimal?** | Daily budget in whole units of &#x60;currency&#x60;. | [optional] 
**LifetimeBudget** | **decimal?** | Lifetime budget in whole units of &#x60;currency&#x60;. | [optional] 
**BudgetMode** | **string** | TikTok only: &#x60;budget_mode&#x60; as TikTok reports it. | [optional] 
**BudgetRemaining** | **decimal?** | Meta &#x60;budget_remaining&#x60; in whole units of &#x60;currency&#x60;. Null when the ad set has no budget of its own, and always on TikTok. | [optional] 
**BidStrategy** | **string** | Meta &#x60;bid_strategy&#x60;. On TikTok the ad group&#39;s &#x60;bid_type&#x60; normalized to the same vocabulary (LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, LOWEST_COST_WITH_MIN_ROAS). | [optional] 
**BidAmount** | **decimal?** | Bid cap or cost target in whole units of &#x60;currency&#x60; (Meta &#x60;bid_amount&#x60;; TikTok &#x60;bid_price&#x60;, else &#x60;conversion_bid_price&#x60;, else &#x60;deep_cpa_bid&#x60;). Null when the strategy has none. | [optional] 
**OptimizationGoal** | **string** | Meta or TikTok &#x60;optimization_goal&#x60;. | [optional] 
**BillingEvent** | **string** | Meta or TikTok &#x60;billing_event&#x60;. | [optional] 
**PromotedObject** | **Dictionary&lt;string, Object&gt;** | Meta &#x60;promoted_object&#x60; verbatim (snake_case). On TikTok &#x60;{ pixelId, customEventType, applicationId, customConversionId }&#x60; from &#x60;pixel_id&#x60;, &#x60;optimization_event&#x60;, &#x60;app_id&#x60; and &#x60;custom_conversion_id&#x60;, only the keys TikTok has set; null when none is. | [optional] 
**Targeting** | **Dictionary&lt;string, Object&gt;** | The platform&#39;s targeting verbatim (snake_case), as it reports it now: Meta &#x60;targeting&#x60;, or TikTok&#39;s ad group targeting fields (location_ids, age_groups, gender, languages, interest_category_ids, audience_ids, placements...). | [optional] 
**Schedule** | [**GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule**](GetAdAccountLiveEntities200ResponseAdSetsInnerSchedule.md) |  | [optional] 
**AdSchedule** | [**List&lt;MetaAdScheduleInner&gt;**](MetaAdScheduleInner.md) | Meta ad set dayparting: the hours the ad set delivers, in whole hours. Same &#x60;dayOfWeek&#x60; / &#x60;startHour&#x60; / &#x60;endHour&#x60; naming as the Google &#x60;PUT /v1/ads/campaigns/{campaignId}/ad-schedule&#x60;, but Meta has no minutes and no bid modifiers. Windows on one day must not overlap (adjacent is fine) and every window must use the same &#x60;timezoneType&#x60;. Invalid windows are a 400 on &#x60;platformSpecificData.adSchedule&#x60;.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

