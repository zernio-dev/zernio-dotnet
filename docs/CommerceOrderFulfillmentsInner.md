# Zernio.Model.CommerceOrderFulfillmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The shipment (fulfillment) id. Entries of one shipment with several tracking numbers share it. | [optional] 
**CarrierName** | **string** |  | [optional] 
**TrackingNumber** | **string** |  | [optional] 
**TrackingUrl** | **string** |  | [optional] 
**DeliveryStatus** | **string** | Where the shipment is. pending means no carrier scan yet. Null when the platform has no delivery tracking for it. Shopify only knows it when the carrier sends tracking events. | [optional] 
**PlatformDeliveryStatus** | **string** | The platform&#39;s raw value, e.g. Shopify ATTEMPTED_DELIVERY. | [optional] 
**EstimatedDeliveryAt** | **DateTime?** |  | [optional] 
**InTransitAt** | **DateTime?** |  | [optional] 
**DeliveredAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

