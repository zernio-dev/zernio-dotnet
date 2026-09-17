# Zernio.Model.Blog
A blog container on the connected platform. All content lives on the platform; Zernio proxies it and stores nothing.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native blog id. Shopify uses a numeric blog id. WordPress.com uses the numeric site id; self-hosted WordPress uses &#x60;1&#x60;, scoped to the connected account. | [optional] 
**Platform** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**Handle** | **string** | URL slug on Shopify; site hostname on WordPress. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

