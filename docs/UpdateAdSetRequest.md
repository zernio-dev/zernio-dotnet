# Zernio.Model.UpdateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**Budget** | [**UpdateAdSetRequestBudget**](UpdateAdSetRequestBudget.md) |  | [optional] 
**Status** | **string** | Writes the ad set&#39;s own on/off switch (Meta: &#x60;configured_status&#x60;) on Meta and LinkedIn, whatever delivery status its ads report. Omit if not toggling delivery state. | [optional] 
**Name** | **string** | Rename the ad set (Meta only; other platforms return 501). At least one of budget/status/bidStrategy/name is required. | [optional] 
**BidStrategy** | **BidStrategy** | Ad-set-level bid strategy. Overrides the campaign-level default. Supported on Meta (facebook, instagram), TikTok, and OpenAI. On TikTok the Meta-style enum is mapped to bid_type / bid_price / deep_bid_type automatically. On OpenAI, LOWEST_COST_WITH_BID_CAP and COST_CAP both map to the ad group&#39;s &#x60;bidding_config.max_bid_micros&#x60; (one knob covers both); LOWEST_COST_WITH_MIN_ROAS is rejected with 422 (OpenAI has no ROAS-based bidding). Other platforms (linkedin, pinterest, google, twitter) return 501 Not Implemented when bidStrategy is set.  | [optional] 
**BidAmount** | **decimal** | Bid cap in WHOLE currency units (USD: 5 &#x3D; $5.00; JPY: 100 &#x3D; ¥100). Required when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. Internally converted to Meta&#39;s smallest-denomination integer, or (on OpenAI) to micros (× 1,000,000). Meta only: may be sent alone, WITHOUT bidStrategy, to update the cap amount on an ad set whose parent campaign is COST_CAP or LOWEST_COST_WITH_BID_CAP (the strategy is inherited from the campaign and is left untouched).  | [optional] 
**RoasAverageFloor** | **decimal** | Minimum ROAS as a decimal multiplier (2.0 &#x3D; 2.0x). Required when bidStrategy is LOWEST_COST_WITH_MIN_ROAS. Sent to Meta as &#x60;bid_constraints.roas_average_floor&#x60; × 10000. Not supported on OpenAI (422).  | [optional] 
**ValueRuleSetId** | **string** | Meta only (other platforms return 501). Value rule set to attach to this ad set, from &#x60;/v1/ads/value-rule-sets&#x60;. Sending a different id replaces the current association. To DETACH, send &#x60;valueRulesApplied: false&#x60; and omit this field.  | [optional] 
**ValueRulesApplied** | **bool** | Meta only (other platforms return 501). &#x60;false&#x60; DETACHES the ad set&#39;s value rule set and must be sent WITHOUT &#x60;valueRuleSetId&#x60;; the combination returns 400. &#x60;true&#x60; is optional when attaching, since attachment is driven by &#x60;valueRuleSetId&#x60;, and requires it to be present.  | [optional] 
**PlatformSpecificData** | [**UpdateAdSetRequestPlatformSpecificData**](UpdateAdSetRequestPlatformSpecificData.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

