# Zernio.Model.UpdateProductRequest
At least one field is required.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | [optional] 
**DescriptionHtml** | **string** | Product description as HTML. | [optional] 
**Handle** | **string** | URL slug of the product. | [optional] 
**Vendor** | **string** |  | [optional] 
**ProductType** | **string** |  | [optional] 
**Tags** | **List&lt;string&gt;** | Replaces the full tag list. | [optional] 
**Status** | **string** | archived hides the product everywhere; draft keeps it editable but unpublished. | [optional] 
**Seo** | [**UpdateProductRequestSeo**](UpdateProductRequestSeo.md) |  | [optional] 
**Variants** | [**List&lt;UpdateProductRequestVariantsInner&gt;**](UpdateProductRequestVariantsInner.md) | Price changes per variant. Only the listed variants change. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

