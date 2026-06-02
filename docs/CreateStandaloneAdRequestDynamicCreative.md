# Zernio.Model.CreateStandaloneAdRequestDynamicCreative
Meta only. Dynamic Creative: supply a POOL of assets and Meta auto-combines and optimises them into the best-performing variations within a single ad (mapped to the creative's `asset_feed_spec`). When set, the top-level single-creative fields (`imageUrl`, `headline`, `body`, `linkUrl`, `callToAction`) are ignored. Mutually exclusive with the `creatives[]` multi-creative shape. Meta limits: ≤10 images, ≤5 bodies / titles / descriptions. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ImageUrls** | **List&lt;string&gt;** | Pool of image URLs (1-10). Uploaded to the ad account and referenced by hash in the asset feed. | 
**Bodies** | **List&lt;string&gt;** | Primary-text variations (the body copy). | [optional] 
**Titles** | **List&lt;string&gt;** | Headline variations. | [optional] 
**Descriptions** | **List&lt;string&gt;** | Description (link caption) variations. | [optional] 
**LinkUrls** | **List&lt;string&gt;** | Destination URL variations. At least one is required unless &#x60;goal&#x60; is &#x60;lead_generation&#x60;. | [optional] 
**CallToActionTypes** | **List&lt;CreateStandaloneAdRequestDynamicCreative.CallToActionTypesEnum&gt;** | CTA-button variations. Required. | [optional] 
**AdFormat** | **string** | Asset-feed ad format. Defaults to SINGLE_IMAGE. | [optional] [default to AdFormatEnum.SINGLEIMAGE]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

