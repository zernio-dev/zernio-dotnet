# Zernio.Model.AmazonSponsoredProductsAdData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdProduct** | **string** |  | 
**TargetingType** | **string** | Required for a new campaign. MANUAL targets keywords and productTargets; AUTO lets Amazon match searches and products (tune them with autoTargeting). Immutable. | [optional] 
**BiddingStrategy** | **string** | Dynamic bidding: LEGACY_FOR_SALES lowers bids when a sale is unlikely, AUTO_FOR_SALES raises and lowers them (up to +100%), MANUAL keeps them fixed. | [optional] [default to BiddingStrategyEnum.LEGACYFORSALES]
**PlacementBidding** | [**List&lt;AmazonSponsoredProductsCampaignDataPlacementBiddingInner&gt;**](AmazonSponsoredProductsCampaignDataPlacementBiddingInner.md) | Bid increase per placement, added on top of the bid (50 on a 1.00 bid gives 1.50 at the top of search). | [optional] 
**PortfolioId** | **string** |  | [optional] 
**Asins** | **List&lt;string&gt;** | Vendor profiles: the ASINs to advertise, one product ad each. | [optional] 
**Skus** | **List&lt;string&gt;** | Seller profiles: the SKUs to advertise, one product ad each. Sending the identifier the profile does not use returns a 400. | [optional] 
**DefaultBid** | **decimal** | Required for a new ad group. Whole currency units; keywords and targets without their own bid use it. US: 0.02 to 1000. | [optional] 
**ProductTargets** | [**List&lt;AmazonSponsoredProductsAdDataAllOfProductTargets&gt;**](AmazonSponsoredProductsAdDataAllOfProductTargets.md) | MANUAL campaigns. Each entry is one Amazon targeting clause: a product (ASIN_SAME_AS), a category (ASIN_CATEGORY_SAME_AS) optionally refined by brand, price, rating or Prime in the same expression. | [optional] 
**NegativeProductTargets** | [**List&lt;AmazonSponsoredProductsAdDataAllOfNegativeProductTargets&gt;**](AmazonSponsoredProductsAdDataAllOfNegativeProductTargets.md) |  | [optional] 
**AutoTargeting** | [**AmazonSponsoredProductsAdDataAllOfAutoTargeting**](AmazonSponsoredProductsAdDataAllOfAutoTargeting.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

