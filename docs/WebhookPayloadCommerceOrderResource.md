# Zernio.Model.WebhookPayloadCommerceOrderResource
Identifiers only, never buyer data: read the order with GET /v1/commerce/orders/{orderId}.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | [optional] 
**Id** | **string** | Platform-native order id. | [optional] 
**Status** | **CommerceOrderStatus** |  | [optional] 
**PlatformStatus** | **string** | Raw platform status, e.g. UNFULFILLED on Shopify or processing on WooCommerce. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

