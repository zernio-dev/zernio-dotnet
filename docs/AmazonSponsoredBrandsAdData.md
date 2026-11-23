# Zernio.Model.AmazonSponsoredBrandsAdData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdProduct** | **string** |  | 
**BrandEntityId** | **string** | The brand (Brand Registry entity) the campaign advertises. Sellers need one. | [optional] 
**BidOptimization** | **bool** | Amazon adjusts placement bids itself. Send false to set placementAdjustments. | [optional] [default to true]
**PlacementAdjustments** | [**List&lt;AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner&gt;**](AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner.md) | Only with bidOptimization false (400 otherwise). | [optional] 
**PortfolioId** | **string** |  | [optional] 
**Ad** | [**AmazonSponsoredBrandsAdDataAllOfAd**](AmazonSponsoredBrandsAdDataAllOfAd.md) |  | [optional] 
**DefaultBid** | **decimal** | Bid of the keywords and product targets without their own. With goal traffic (cost per click), US: 0.10 to 49, video 0.25 to 49. | [optional] 
**ProductTargets** | [**List&lt;AmazonSponsoredBrandsAdDataAllOfProductTargets&gt;**](AmazonSponsoredBrandsAdDataAllOfProductTargets.md) |  | [optional] 
**NegativeProductTargets** | [**List&lt;AmazonSponsoredBrandsAdDataAllOfNegativeProductTargets&gt;**](AmazonSponsoredBrandsAdDataAllOfNegativeProductTargets.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

