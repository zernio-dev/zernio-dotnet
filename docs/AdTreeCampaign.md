# Zernio.Model.AdTreeCampaign
Campaign with nested ad sets and rolled-up metrics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlatformCampaignId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**CampaignName** | **string** |  | [optional] 
**Status** | **AdStatus** | Delivery status derived from child ad statuses. Distinct from &#x60;reviewStatus&#x60;, which reflects the platform-side review state. | [optional] 
**ReviewStatus** | **AdReviewStatus** |  | [optional] 
**PlatformCampaignStatus** | **string** | Raw platform-level campaign status (Meta &#x60;effective_status&#x60;: ACTIVE, PAUSED, DELETED, ARCHIVED, IN_PROCESS, WITH_ISSUES). Distinct from per-ad &#x60;platformStatus&#x60;. | [optional] 
**CampaignIssuesInfo** | **List&lt;Object&gt;** | Platform-reported campaign issues (Meta &#x60;issues_info[]&#x60;). Populated only when the platform has delivery issues to report; contains the specific error codes and messages. | [optional] 
**AdCount** | **int** | Total ads across all ad sets | [optional] 
**AdSetCount** | **int** |  | [optional] 
**Budget** | [**AdTreeCampaignBudget**](AdTreeCampaignBudget.md) |  | [optional] 
**CampaignBudget** | [**AdTreeCampaignCampaignBudget**](AdTreeCampaignCampaignBudget.md) |  | [optional] 
**BudgetLevel** | **string** | Canonical CBO/ABO indicator. &#x60;campaign&#x60; &#x3D; CBO (Advantage Campaign Budget, budget lives on the campaign). &#x60;adset&#x60; &#x3D; ABO (budget lives on each ad set). Route budget updates to the matching Meta entity. | [optional] 
**IsBudgetScheduleEnabled** | **bool** | Meta-only. Mirrors Campaign.is_budget_schedule_enabled — true when the campaign uses budget scheduling (time-based budget changes). Independent of CBO/ABO. | [optional] [default to false]
**Currency** | **string** | ISO 4217 currency code (e.g. USD, EUR, CLP, JPY) for all budget amounts in this campaign node. Budgets are NOT normalized to USD. | [optional] 
**Metrics** | [**AdMetrics**](AdMetrics.md) |  | [optional] 
**PlatformAdAccountId** | **string** |  | [optional] 
**PlatformAdAccountName** | **string** | Human-readable advertiser/account name from the platform. Refreshed on every sync. | [optional] 
**AccountId** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**AdvertisingChannelType** | **string** | Google-only. Raw campaign.advertising_channel_type (SEARCH, PERFORMANCE_MAX, VIDEO, DEMAND_GEN, DISPLAY, SHOPPING, ...). Serving surface, distinct from platformObjective (advertiser intent). Null/absent for non-Google platforms. | [optional] 
**PlatformObjective** | **string** | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC) | [optional] 
**OptimizationGoal** | **string** | Meta optimization goal shared across ad sets, or comma-separated values when ad sets differ (e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION) | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal?** | Representative bid cap for the campaign — bubbled up from the top-spending ad set&#39;s &#x60;bid_amount&#x60; (whole currency units). Populated when the ad-set bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. | [optional] 
**RoasAverageFloor** | **decimal?** | Representative ROAS floor for the campaign — bubbled up from the top-spending ad set. Decimal multiplier (2.0 &#x3D; 2.0x). | [optional] 
**PromotedObject** | [**AdTreeCampaignPromotedObject**](AdTreeCampaignPromotedObject.md) |  | [optional] 
**AdSets** | [**List&lt;AdTreeAdSet&gt;**](AdTreeAdSet.md) |  | [optional] 
**Daily** | [**List&lt;AdDailyMetrics&gt;**](AdDailyMetrics.md) | Per-day metric series for this campaign. Present only when &#x60;GET /v1/ads/tree&#x60; is called with &#x60;timeIncrement&#x3D;1&#x60; (any &#x60;dailyLevel&#x60;). This is the per-campaign daily trend — summing its additive fields reproduces the campaign &#x60;metrics&#x60; total. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

