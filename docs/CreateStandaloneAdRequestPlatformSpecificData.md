# Zernio.Model.CreateStandaloneAdRequestPlatformSpecificData
Platform-specific options. The platform is derived from `accountId`; sending options for a different platform returns a 400. LinkedIn (campaign bidding and delivery controls) and Meta (the bid trio) have options today.  **Meta**: `bidStrategy`, `bidAmount` and `roasAverageFloor` may be sent here instead of at the root — the preferred home going forward. Sending the bid fields in BOTH places returns a 400 (`mutually_exclusive_fields`), and sending any of them in `adSetId` attach mode is a 400 too (the ad set already has its bid). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CostType** | **string** | Campaign cost model (billing event). Defaults to &#x60;CPM&#x60;. Required when &#x60;unitCost&#x60; is set so the manual bid applies to an explicit cost model.  | [optional] 
**UnitCost** | **decimal** | Manual bid in WHOLE account-currency units (e.g. 2.5 &#x3D; $2.50). Requires &#x60;costType&#x60;. Omit for LinkedIn&#39;s automated (max delivery) bidding. LinkedIn enforces its own per-audience min/max bid bounds.  | [optional] 
**OptimizationTargetType** | **string** | Campaign &#x60;optimizationTargetType&#x60; (e.g. &#x60;MAX_CLICK&#x60;, &#x60;TARGET_COST_PER_CLICK&#x60;, &#x60;MAX_IMPRESSION&#x60;). Forwarded verbatim, LinkedIn validates compatibility with the objective and &#x60;costType&#x60;. Omit for the objective-derived default: &#x60;awareness&#x60; gets &#x60;MAX_IMPRESSION&#x60;, &#x60;video_views&#x60; gets &#x60;MAX_VIDEO_VIEW&#x60;, and every other goal gets &#x60;MAX_CLICK&#x60;. &#x60;lead_generation&#x60; and &#x60;conversions&#x60; also get &#x60;MAX_CLICK&#x60;, because &#x60;MAX_LEAD&#x60; and &#x60;MAX_CONVERSION&#x60; need a lead gen form or a conversion rule that neither creation flow attaches. The default applies only to &#x60;SPONSORED_UPDATES&#x60; campaigns (every boost, and the image, video and carousel standalone ads), never to the &#x60;TEXT_AD&#x60;, &#x60;DYNAMIC&#x60; and &#x60;SPONSORED_INMAILS&#x60; campaigns the other creative formats produce. It is also skipped when &#x60;unitCost&#x60; or a non-&#x60;CPM&#x60; &#x60;costType&#x60; is set, since those select manual bidding and the bid is then yours to choose.  | [optional] 
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
**BidAmount** | **decimal** | Whole currency units (USD: 5 &#x3D; $5.00). Required when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. May also be sent alone, WITHOUT bidStrategy, to set the cap on an ad set joining a COST_CAP / LOWEST_COST_WITH_BID_CAP campaign (the strategy is inherited from the campaign). On POST /v1/ads/create that shape requires existingCampaignId and is a 400 otherwise; on POST /v1/ads/boost it is promoted to LOWEST_COST_WITH_BID_CAP. | [optional] 
**RoasAverageFloor** | **decimal** | Decimal ROAS multiplier (2.0 &#x3D; 2.0x). Required when bidStrategy is LOWEST_COST_WITH_MIN_ROAS; sending it without bidStrategy is a 400. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

