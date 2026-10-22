# Zernio.Model.CommerceOrderAttribution
Where the order came from. Shopify reads it from the customer journey, WooCommerce from its order attribution (WooCommerce 8.5+ with the feature on, orders placed after it was turned on).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ready** | **bool** | False while Shopify is still attributing a new order. No webhook fires when it becomes true, so read the order again later. Always true on WooCommerce. | [optional] 
**FirstVisit** | [**CommerceOrderVisit**](CommerceOrderVisit.md) |  | [optional] 
**LastVisit** | [**CommerceOrderVisit**](CommerceOrderVisit.md) |  | [optional] 
**CustomAttributes** | [**List&lt;BoostPostRequestTrackingUrlTagsInner&gt;**](BoostPostRequestTrackingUrlTagsInner.md) | Shopify cart and note attributes, or WooCommerce public order meta. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

