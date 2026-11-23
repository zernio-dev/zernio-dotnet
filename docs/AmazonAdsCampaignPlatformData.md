# Zernio.Model.AmazonAdsCampaignPlatformData
Amazon Ads: the ad product of the campaign and its settings. Unknown keys return a 400.  The unified `goal` maps onto the product: Sponsored Products takes `conversions`; Sponsored Brands takes `traffic` (PAGE_VISIT), `awareness` (BRAND_IMPRESSION_SHARE), `video_views` (AD_VIEWS) and `conversions` (ACQUIRE_NEW_CUSTOMERS); Sponsored Display takes `traffic` (optimizes for clicks), `conversions` and `awareness` (optimizes for reach and bills by viewable impressions). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdProduct** | **string** |  | 
**TargetingType** | **string** | Required for a new campaign. MANUAL targets keywords and productTargets; AUTO lets Amazon match searches and products (tune them with autoTargeting). Immutable. | [optional] 
**BiddingStrategy** | **string** | Dynamic bidding: LEGACY_FOR_SALES lowers bids when a sale is unlikely, AUTO_FOR_SALES raises and lowers them (up to +100%), MANUAL keeps them fixed. | [optional] [default to BiddingStrategyEnum.LEGACYFORSALES]
**PlacementBidding** | [**List&lt;AmazonSponsoredProductsCampaignDataPlacementBiddingInner&gt;**](AmazonSponsoredProductsCampaignDataPlacementBiddingInner.md) | Bid increase per placement, added on top of the bid (50 on a 1.00 bid gives 1.50 at the top of search). | [optional] 
**PortfolioId** | **string** |  | [optional] 
**BrandEntityId** | **string** | The brand (Brand Registry entity) the campaign advertises. Sellers need one. | [optional] 
**BidOptimization** | **bool** | Amazon adjusts placement bids itself. Send false to set placementAdjustments. | [optional] [default to true]
**PlacementAdjustments** | [**List&lt;AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner&gt;**](AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner.md) | Only with bidOptimization false (400 otherwise). | [optional] 
**Tactic** | **string** | Required for a new campaign. T00020 targets products and categories; T00030 also targets audiences (views, purchases, audience). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

