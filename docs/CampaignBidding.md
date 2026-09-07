# Zernio.Model.CampaignBidding
A Google campaign's current bidding, mapped onto the same triplet PUT /v1/ads/campaigns/{campaignId} accepts.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Channel** | **string** | campaign.advertising_channel_type. COST_CAP&#39;s underlying Google field differs by channel; see bidStrategy on PUT. | [optional] 
**BiddingStrategyType** | **string** | Google&#39;s raw enum: MAXIMIZE_CONVERSIONS, TARGET_CPA, MAXIMIZE_CONVERSION_VALUE, TARGET_ROAS, TARGET_SPEND, MANUAL_CPC, TARGET_IMPRESSION_SHARE, or another Google adds later. | [optional] 
**BidSpec** | [**CampaignBiddingBidSpec**](CampaignBiddingBidSpec.md) |  | [optional] 
**Portfolio** | [**CampaignBiddingPortfolio**](CampaignBiddingPortfolio.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

