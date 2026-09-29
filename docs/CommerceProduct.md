# Zernio.Model.CommerceProduct
A product on a connected store, in the platform-neutral shape.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native product id. | [optional] 
**AccountId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**DescriptionHtml** | **string** |  | [optional] 
**Handle** | **string** | URL slug of the product. | [optional] 
**Vendor** | **string** |  | [optional] 
**ProductType** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**Status** | **CommerceProductStatus** |  | [optional] 
**PlatformStatus** | **string** | The raw status on the platform, e.g. ACTIVE on Shopify. | [optional] 
**FeaturedImage** | [**CommerceImage**](CommerceImage.md) |  | [optional] 
**Images** | [**List&lt;CommerceImage&gt;**](CommerceImage.md) | First 20 images, in store order. | [optional] 
**Options** | [**List&lt;ProductOptionsInner&gt;**](ProductOptionsInner.md) | Option axes (e.g. Size, Color) and their values. | [optional] 
**Variants** | [**List&lt;CommerceVariant&gt;**](CommerceVariant.md) | First 100 variants. | [optional] 
**TotalInventory** | **int?** |  | [optional] 
**Url** | **string** | Public storefront URL; null while the product is not published. | [optional] 
**Seo** | [**ProductSeo**](ProductSeo.md) |  | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 
**UpdatedAt** | **DateTime?** |  | [optional] 
**PublishedAt** | **DateTime?** |  | [optional] 
**PlatformData** | **Dictionary&lt;string, Object&gt;** | Platform-only fields. Null when the platform has none. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

