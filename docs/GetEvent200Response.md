# Zernio.Model.GetEvent200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Event** | [**StoredEvent**](StoredEvent.md) |  | [optional] 
**Deliveries** | [**List&lt;GetEvent200ResponseDeliveriesInner&gt;**](GetEvent200ResponseDeliveriesInner.md) |  | [optional] 
**Touches** | [**List&lt;GetEvent200ResponseTouchesInner&gt;**](GetEvent200ResponseTouchesInner.md) | The touches the event is split across, oldest first: website visits (an ad click, search, a tagged link), the first and latest visits HubSpot recorded for a deal, earlier lead forms or sales, and a Shopify buyer&#39;s post-purchase survey answer. Empty when the event counts whole for its own campaign. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

