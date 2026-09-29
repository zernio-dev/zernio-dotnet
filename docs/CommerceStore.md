# Zernio.Model.CommerceStore

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id of the store. | 
**Platform** | **string** |  | 
**Name** | **string** |  | 
**Domain** | **string** | The platform domain of the store, e.g. my-store.myshopify.com. | 
**Url** | **string** | Public storefront URL. | 
**Currency** | **string** | ISO 4217 code the store sells in. | 
**Country** | **string** | ISO 3166-1 alpha-2 country of the store. | 
**Capabilities** | [**List&lt;CommerceCapability&gt;**](CommerceCapability.md) |  | 
**MissingCapabilities** | [**List&lt;CommerceCapability&gt;**](CommerceCapability.md) | Capabilities the platform supports that this store has not granted yet. | 
**GrantPermissionsUrl** | **string** | Shopify: a page in the Shopify admin where the store owner approves the permissions missingCapabilities need, on the existing install (no reinstall; they can revoke them later). Null when nothing is missing or the store cannot grant them this way (a store connected with its own custom-app token). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

