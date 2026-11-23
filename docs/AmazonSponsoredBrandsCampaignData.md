# Zernio.Model.AmazonSponsoredBrandsCampaignData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdProduct** | **string** |  | 
**BrandEntityId** | **string** | The brand (Brand Registry entity) the campaign advertises. Sellers need one. | [optional] 
**BidOptimization** | **bool** | Amazon adjusts placement bids itself. Send false to set placementAdjustments. | [optional] [default to true]
**PlacementAdjustments** | [**List&lt;AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner&gt;**](AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner.md) | Only with bidOptimization false (400 otherwise). | [optional] 
**PortfolioId** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

