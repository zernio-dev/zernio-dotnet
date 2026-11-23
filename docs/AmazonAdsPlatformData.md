# Zernio.Model.AmazonAdsPlatformData
Amazon Ads (required): the ad product and everything the unified fields do not cover. Unknown keys return a 400.  Unified fields that apply:  - `name`, `campaignName`, `adSetName`, `adName`, `goal` and the status fields. - `budgetAmount` / `budgetType`: the campaign budget in whole currency units; lifetime on Sponsored Brands only. - `startDate` / `endDate`: calendar days in the profile time zone. - `keywords` and `negativeKeywords` (Sponsored Products and Brands), `campaignNegativeKeywords` (Sponsored Products). - `existingCampaignId`: a new ad group under an existing campaign of the same product, which keeps its goal when `goal` is omitted. - `adSetId`: new ads in an existing ad group.  Creative and audience fields (headline, body, linkUrl, imageUrl, countries, interests...) return a 400.  Goals per product are listed on `AmazonAdsCampaignPlatformData`. If anything after the campaign fails, the campaign is archived (Amazon's delete) and the error names the refused item, e.g. `keywords[2]`. 

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
**DefaultBid** | **decimal** | US: 0.02 to 1000 per click, 1 to 1000 per thousand viewable impressions (goal awareness). | [optional] 
**ProductTargets** | [**List&lt;AmazonSponsoredBrandsAdDataAllOfProductTargets&gt;**](AmazonSponsoredBrandsAdDataAllOfProductTargets.md) |  | [optional] 
**NegativeProductTargets** | [**List&lt;AmazonSponsoredBrandsAdDataAllOfNegativeProductTargets&gt;**](AmazonSponsoredBrandsAdDataAllOfNegativeProductTargets.md) |  | [optional] 
**AutoTargeting** | [**AmazonSponsoredProductsAdDataAllOfAutoTargeting**](AmazonSponsoredProductsAdDataAllOfAutoTargeting.md) |  | [optional] 
**BrandEntityId** | **string** | The brand (Brand Registry entity) the campaign advertises. Sellers need one. | [optional] 
**BidOptimization** | **bool** | Amazon adjusts placement bids itself. Send false to set placementAdjustments. | [optional] [default to true]
**PlacementAdjustments** | [**List&lt;AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner&gt;**](AmazonSponsoredBrandsCampaignDataPlacementAdjustmentsInner.md) | Only with bidOptimization false (400 otherwise). | [optional] 
**Ad** | [**AmazonSponsoredBrandsAdDataAllOfAd**](AmazonSponsoredBrandsAdDataAllOfAd.md) |  | [optional] 
**Tactic** | **string** | Required for a new campaign. T00020 targets products and categories; T00030 also targets audiences (views, purchases, audience). | [optional] 
**Targets** | [**List&lt;AmazonSponsoredDisplayAdDataAllOfTargets&gt;**](AmazonSponsoredDisplayAdDataAllOfTargets.md) | Required for a new ad group. Each entry is one Amazon targeting clause, in Amazon&#39;s own shape:  - Contextual: &#x60;{ type: similarProduct }&#x60;, &#x60;{ type: asinSameAs, value: B0... }&#x60;, &#x60;{ type: asinCategorySameAs, value: \&quot;12345\&quot; }&#x60; with optional brand, price or rating refinements in the same expression, &#x60;{ type: contentCategorySameAs, value: \&quot;amzn1.iab-content.325\&quot; }&#x60;. - Audiences (tactic T00030 only): &#x60;{ type: views | purchases, value: [{ type: exactProduct | similarProduct | relatedProduct | asinCategorySameAs ... }, { type: lookback, value: \&quot;30\&quot; }] }&#x60;, or &#x60;{ type: audience, value: [{ type: audienceSameAs, value: \&quot;&lt;audience id&gt;\&quot; }] }&#x60; for in-market and lifestyle audiences.  | [optional] 
**NegativeTargets** | [**List&lt;AmazonSponsoredBrandsAdDataAllOfNegativeProductTargets&gt;**](AmazonSponsoredBrandsAdDataAllOfNegativeProductTargets.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

