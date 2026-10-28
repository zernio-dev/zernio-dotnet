# Zernio.Model.CreateAdCatalogRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | A facebook, instagram, metaads or whatsapp account ID | 
**CatalogAccountId** | **string** | Account whose Meta login token performs the call (see GET) | [optional] 
**AdAccountId** | **string** | Ad account whose owner business creates the catalog | [optional] 
**BusinessId** | **string** | Business portfolio that owns the catalog | [optional] 
**Name** | **string** |  | 
**Vertical** | **string** | Meta catalog vertical. Use services for a professional services catalog (for example one linked to WhatsApp). local_service_business is a deprecated alias of local_service_businesses. The product endpoints under /v1/ads/catalogs/{catalogId}/products write commerce product items only. | [optional] [default to VerticalEnum.Commerce]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

