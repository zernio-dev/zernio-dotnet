# Zernio.Model.CreateStandaloneAdRequestPlatformSpecificData
Platform-specific options. The platform is derived from `accountId`; options for a different platform return a 400. LinkedIn (campaign bidding and delivery controls), Meta (the bid trio) Amazon Ads (required: the ad product, products, creative and targeting) and AppLovin (the campaign and creative set) have options today.  **Amazon Ads**: see `AmazonAdsPlatformData`. Amazon has no dry run, so `validateOnly` returns a 501.  **AppLovin**  - A new campaign needs `campaignType` (`APP` or `WEB`), the goal and, for an app, `os`, `packageName` and `tracking`. With `existingCampaignId`, only the creative set fields (`assets`, `languages`, `brandInfo`) apply. - Zernio checks every documented AppLovin rule (goal value limits, ROAS day targets, US-only regions and metros, the asset combination, brand info lengths) before calling AppLovin, because 100 refused calls in five minutes lock the AppLovin account for a day. `validateOnly` runs those checks and calls nothing.  **Meta**  - `bidStrategy`, `bidAmount` and `roasAverageFloor` may be sent here instead of at the root (the preferred home going forward). Sending them in BOTH places returns a 400 (`mutually_exclusive_fields`). - Sending any bid field in `adSetId` attach mode is a 400 (the ad set already has its bid). - `dailyMinSpendTarget` / `lifetimeMinSpendTarget` set the new ad set's minimum spend and live here only; also rejected in `adSetId` attach mode. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CostType** | **string** | Campaign cost model (billing event). Defaults to &#x60;CPM&#x60;. Required when &#x60;unitCost&#x60; is set so the manual bid applies to an explicit cost model.  | [optional] 
**UnitCost** | **decimal** | Manual bid in WHOLE account-currency units (e.g. 2.5 &#x3D; $2.50). Requires &#x60;costType&#x60;. Omit for LinkedIn&#39;s automated (max delivery) bidding. LinkedIn enforces its own per-audience min/max bid bounds.  | [optional] 
**OptimizationTargetType** | **string** | Campaign &#x60;optimizationTargetType&#x60; (e.g. &#x60;MAX_CLICK&#x60;, &#x60;TARGET_COST_PER_CLICK&#x60;, &#x60;MAX_IMPRESSION&#x60;). Forwarded verbatim; LinkedIn validates compatibility with the objective and &#x60;costType&#x60;.  **Default** when omitted, derived from the objective:  - &#x60;awareness&#x60;: &#x60;MAX_IMPRESSION&#x60;. - &#x60;video_views&#x60;: &#x60;MAX_VIDEO_VIEW&#x60;. - Every other goal: &#x60;MAX_CLICK&#x60;. That includes &#x60;lead_generation&#x60; and &#x60;conversions&#x60;, because &#x60;MAX_LEAD&#x60; and &#x60;MAX_CONVERSION&#x60; need a lead gen form or a conversion rule that neither creation flow attaches.  The default applies only to &#x60;SPONSORED_UPDATES&#x60; campaigns (every boost, and the image, video and carousel standalone ads), never to the &#x60;TEXT_AD&#x60;, &#x60;DYNAMIC&#x60; and &#x60;SPONSORED_INMAILS&#x60; campaigns the other creative formats produce.  It is also skipped when &#x60;unitCost&#x60; or a non-&#x60;CPM&#x60; &#x60;costType&#x60; is set, since those select manual bidding and the bid is then yours to choose.  | [optional] 
**CreativeSelection** | **string** | How LinkedIn rotates creatives within the campaign. Defaults to &#x60;OPTIMIZED&#x60;. | [optional] 
**AudienceExpansionEnabled** | **bool** | Enable LinkedIn audience expansion. Defaults to false. | [optional] 
**OffsiteDeliveryEnabled** | **bool** | Deliver on the LinkedIn Audience Network. Defaults to false. | [optional] 
**ConnectedTelevisionOnly** | **bool** | Restrict delivery to Connected TV inventory. | [optional] 
**Carousel** | [**LinkedInAdsPlatformDataCarousel**](LinkedInAdsPlatformDataCarousel.md) |  | [optional] 
**Document** | [**LinkedInAdsPlatformDataDocument**](LinkedInAdsPlatformDataDocument.md) |  | [optional] 
**Spotlight** | [**LinkedInAdsPlatformDataSpotlight**](LinkedInAdsPlatformDataSpotlight.md) |  | [optional] 
**Follower** | [**LinkedInAdsPlatformDataFollower**](LinkedInAdsPlatformDataFollower.md) |  | [optional] 
**Jobs** | [**LinkedInAdsPlatformDataJobs**](LinkedInAdsPlatformDataJobs.md) |  | [optional] 
**TextAd** | [**LinkedInAdsPlatformDataTextAd**](LinkedInAdsPlatformDataTextAd.md) |  | [optional] 
**Conversation** | [**LinkedInAdsPlatformDataConversation**](LinkedInAdsPlatformDataConversation.md) |  | [optional] 
**Event** | [**LinkedInAdsPlatformDataEvent**](LinkedInAdsPlatformDataEvent.md) |  | [optional] 
**ThoughtLeader** | [**LinkedInAdsPlatformDataThoughtLeader**](LinkedInAdsPlatformDataThoughtLeader.md) |  | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal** | Whole currency units (USD: 5 &#x3D; $5.00). Required when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP.  May also be sent alone, WITHOUT bidStrategy, to set the cap on an ad set joining a COST_CAP / LOWEST_COST_WITH_BID_CAP campaign (the strategy is inherited from the campaign):  - POST /v1/ads/create: that shape requires existingCampaignId and is a 400 otherwise. - POST /v1/ads/boost: it is promoted to LOWEST_COST_WITH_BID_CAP. | [optional] 
**RoasAverageFloor** | **decimal** | Decimal ROAS multiplier (2.0 &#x3D; 2.0x). Required when bidStrategy is LOWEST_COST_WITH_MIN_ROAS; sending it without bidStrategy is a 400. | [optional] 
**DailyMinSpendTarget** | **decimal** | Meta daily_min_spend_target on the ad set being created: the least it should spend per day, in whole currency units. A target, not a guarantee.  - It reserves a share of a CAMPAIGN budget, so it requires budgetLevel campaign or an existingCampaignId whose campaign has the budget (Advantage campaign budget / CBO). With an ad-set budget it is a 400 (Meta rejects a spend limit on an ad set that owns its budget). - Mutually exclusive with lifetimeMinSpendTarget: the flavour must match the campaign budget type. - Rejected with 400 on POST /v1/ads/boost and in adSetId attach mode: use PUT /v1/ads/ad-sets/{adSetId} for an existing ad set. | [optional] 
**LifetimeMinSpendTarget** | **decimal** | Meta lifetime_min_spend_target: the lifetime-budget flavour of dailyMinSpendTarget, in whole currency units. Same rules and same rejections. | [optional] 
**CustomerLifecycle** | [**MetaCustomerLifecycle**](MetaCustomerLifecycle.md) |  | [optional] 
**AdSchedule** | [**List&lt;MetaAdScheduleInner&gt;**](MetaAdScheduleInner.md) | Dayparting on the ad set being created (Meta &#x60;adset_schedule&#x60; with &#x60;pacing_type: [\&quot;day_parting\&quot;]&#x60;). Change it later with &#x60;PUT /v1/ads/ad-sets/{adSetId}&#x60;.  A 400 with &#x60;param: platformSpecificData.adSchedule&#x60; when:  - the budget is daily (on the ad set, or on the campaign joined with &#x60;existingCampaignId&#x60;): Meta runs a schedule only on a LIFETIME budget. - the value is empty. - in adSetId attach mode. - with &#x60;buyingType: RESERVED&#x60;.  | [optional] 
**CampaignType** | **string** | Required for a new campaign. | [optional] 
**Os** | **string** | APP campaigns. Required. | [optional] 
**PackageName** | **string** | APP campaigns. Required. | [optional] 
**ItunesId** | **int** | iOS APP campaigns. Required. | [optional] 
**WebsiteUrl** | **string** | WEB campaigns. Required unless linkUrl is sent. | [optional] 
**BiddingStrategy** | **string** | Defaults to CPI billing for a CPI goal, CPM billing otherwise. TARGET_GOAL_WITH_CPI_BILLING takes an APP campaign with a CPI goal only. Set at creation only. | [optional] 
**GoalType** | **string** | APP takes all, WEB takes CPE, CPP and CHK_ROAS. Defaults from goal: app_promotion is CPI, conversions CPP, lead_generation CPE. Set at creation only. | [optional] 
**GoalValue** | **decimal** | The goal for every country (a cost, or a ROAS ratio). APP limits: CPI below 200, CPE and CPP below 500, AD_ROAS at least 0.1, CHK_ROAS at least 0.01, BLD_ROAS at least 0.05. Send this or countryGoalValues. | [optional] 
**CountryGoalValues** | **Dictionary&lt;string, decimal&gt;** | Per-country goal values for targeted countries. | [optional] 
**RoasDayTarget** | **string** | Required for ROAS goals (and WEB CPP). APP takes DAY7 or DAY28, WEB DAY0 or DAY7. | [optional] 
**EventTarget** | **string** | Required for a CPE goal. | [optional] 
**CountryBudgets** | **Dictionary&lt;string, decimal&gt;** | Per-country daily budgets, instead of budgetAmount. AppLovin budgets are daily only. | [optional] 
**Tracking** | [**AppLovinAdsPlatformDataTracking**](AppLovinAdsPlatformDataTracking.md) |  | [optional] 
**AudienceStrategy** | **string** | WEB campaigns. | [optional] 
**Assets** | [**List&lt;AppLovinAdsPlatformDataAssetsInner&gt;**](AppLovinAdsPlatformDataAssetsInner.md) | The creative set media: URLs Zernio uploads to AppLovin, or ids of assets already there. Needs a HOSTED_HTML asset, or an IMG_INTER_P image plus a VID_LONG_P or VID_SHORT_P video. | [optional] 
**Languages** | **List&lt;string&gt;** | Creative set languages as AppLovin names them. All languages by default. | [optional] 
**BrandInfo** | [**AppLovinAdsPlatformDataBrandInfo**](AppLovinAdsPlatformDataBrandInfo.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

