# Zernio.Model.CampaignBiddingBidSpec
Null when the campaign is on a strategy PUT does not model (Manual CPC, Target Impression Share, ...); show biddingStrategyType instead in that case.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal** | Whole currency units. Present for COST_CAP and LOWEST_COST_WITH_BID_CAP, and omitted when the campaign is on a bare TARGET_SPEND with no CPC ceiling set. | [optional] 
**RoasAverageFloor** | **decimal** | Decimal ROAS multiplier (2.0 &#x3D; 2.0x). Present for LOWEST_COST_WITH_MIN_ROAS. | [optional] 
**PortfolioBidStrategyId** | **string** | Present alone (bidStrategy omitted) when the campaign is on a portfolio strategy; see portfolio. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

