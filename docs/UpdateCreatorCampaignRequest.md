# Zernio.Model.UpdateCreatorCampaignRequest
Every field is optional; send at least one. `economics` can only change while the campaign is a draft.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**BrandName** | **string** |  | [optional] 
**Platforms** | **List&lt;UpdateCreatorCampaignRequest.PlatformsEnum&gt;** |  | [optional] 
**ContentRules** | **string** |  | [optional] 
**StartsAt** | **DateTime?** |  | [optional] 
**EndsAt** | **DateTime?** |  | [optional] 
**TrackingDays** | **int** |  | [optional] 
**HoldDays** | **int** |  | [optional] 
**MaxPostAgeMinutes** | **int?** | Null removes the limit. | [optional] 
**Settlement** | **string** |  | [optional] 
**Economics** | [**CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | [optional] 
**Caps** | [**CreatorCampaignCaps**](CreatorCampaignCaps.md) |  | [optional] 
**Branding** | [**CreatorCampaignBranding**](CreatorCampaignBranding.md) |  | [optional] 
**LandingUrl** | **string** | The page creator tracking links open. Required unless &#x60;attribution&#x60; is &#x60;code&#x60;. | [optional] 
**CodeDiscountPercent** | **int?** | What each creator&#39;s discount code takes off an order. Required unless &#x60;attribution&#x60; is &#x60;link&#x60;. | [optional] 
**JoinApproval** | **string** | manual holds creators who join through the open link as &#x60;pending&#x60; until you approve them. Personal invites are never held. | [optional] 
**RequireDraftApproval** | **bool** | Creators upload a draft for review before publishing, and each submitted post must name an approved draft. | [optional] 
**StoreAccountId** | **string** | A connected Shopify or WooCommerce store account. On &#x60;commission&#x60; and smart &#x60;retainer&#x60; economics its orders pay commission: required there, and fixed once such a campaign leaves draft.  On any campaign creators can ask for free samples of its products (&#x60;sampleProductIds&#x60;). Changing it without &#x60;sampleProductIds&#x60; clears the sample products; null removes the store and the products.  | [optional] 
**SampleProductIds** | **List&lt;string&gt;** | Product ids in the store that creators can ask a free sample of. Each is read from the store and saved as &#x60;sampleProducts&#x60;; an unknown product answers 404 &#x60;product_not_found&#x60;. Needs a store, otherwise 400 &#x60;missing_required_field&#x60; (&#x60;param: storeAccountId&#x60;). | [optional] 
**SampleContentDueDays** | **int** | Days after a sample is approved before a creator with no post since shows as owing content. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

