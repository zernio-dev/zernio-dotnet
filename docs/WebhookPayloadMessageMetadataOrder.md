# Zernio.Model.WebhookPayloadMessageMetadataOrder
WhatsApp only. Cart submitted by the user from a commerce message (catalog, product, or product-list message). Meta's `order` object forwarded verbatim. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CatalogId** | **string** | Meta catalog the ordered products belong to. | [optional] 
**Text** | **string** | Optional free-text note the user attached to the cart. | [optional] 
**ProductItems** | [**List&lt;WebhookPayloadMessageMetadataOrderProductItemsInner&gt;**](WebhookPayloadMessageMetadataOrderProductItemsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

