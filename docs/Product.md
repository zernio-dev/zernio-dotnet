# Zernio.Model.Product
A product on the connected platform with its variants, options and images. All data lives on the platform; Zernio proxies it and stores nothing.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native product id (numeric string for Shopify). | [optional] 
**Platform** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**Handle** | **string** | URL slug of the product. | [optional] 
**DescriptionHtml** | **string** | Product description as HTML. | [optional] 
**Vendor** | **string** |  | [optional] 
**ProductType** | **string** | Free-text product type as set on the store. | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**Status** | **string** |  | [optional] 
**FeaturedImage** | [**ProductImage**](ProductImage.md) |  | [optional] 
**Images** | [**List&lt;ProductImage&gt;**](ProductImage.md) | First 20 images in the product media, in store order. | [optional] 
**Options** | [**List&lt;ProductOptionsInner&gt;**](ProductOptionsInner.md) | Option axes (e.g. Size, Color) and their values. | [optional] 
**Variants** | [**List&lt;ProductVariant&gt;**](ProductVariant.md) | First 100 variants. | [optional] 
**Seo** | [**ProductSeo**](ProductSeo.md) |  | [optional] 
**TotalInventory** | **int?** |  | [optional] 
**OnlineStoreUrl** | **string** | Public storefront URL; null while the product is not published to the online store. | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 
**UpdatedAt** | **DateTime?** |  | [optional] 
**PublishedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

