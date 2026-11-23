# Zernio.Model.AmazonSponsoredProductsCampaignData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdProduct** | **string** |  | 
**TargetingType** | **string** | Required for a new campaign. MANUAL targets keywords and productTargets; AUTO lets Amazon match searches and products (tune them with autoTargeting). Immutable. | [optional] 
**BiddingStrategy** | **string** | Dynamic bidding: LEGACY_FOR_SALES lowers bids when a sale is unlikely, AUTO_FOR_SALES raises and lowers them (up to +100%), MANUAL keeps them fixed. | [optional] [default to BiddingStrategyEnum.LEGACYFORSALES]
**PlacementBidding** | [**List&lt;AmazonSponsoredProductsCampaignDataPlacementBiddingInner&gt;**](AmazonSponsoredProductsCampaignDataPlacementBiddingInner.md) | Bid increase per placement, added on top of the bid (50 on a 1.00 bid gives 1.50 at the top of search). | [optional] 
**PortfolioId** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

