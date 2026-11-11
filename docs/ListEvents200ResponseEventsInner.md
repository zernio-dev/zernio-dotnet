# Zernio.Model.ListEvents200ResponseEventsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventId** | **string** |  | [optional] 
**Source** | **string** | Where the event came from: &#x60;api&#x60;, &#x60;relay&#x60;, &#x60;web&#x60;, &#x60;shopify&#x60;, &#x60;woocommerce&#x60;, &#x60;hubspot&#x60;, &#x60;meta_leads&#x60;, &#x60;google_leads&#x60;, &#x60;linkedin_leads&#x60; or &#x60;tiktok_leads&#x60;. | [optional] 
**EventName** | **string** |  | [optional] 
**EventTime** | **DateTime** |  | [optional] 
**ReceivedAt** | **DateTime** |  | [optional] 
**ActionSource** | **string** |  | [optional] 
**Value** | **decimal** |  | [optional] 
**Currency** | **string** |  | [optional] 
**SourceUrl** | **string** | Origin, path and attribution parameters only. | [optional] 
**Utm** | [**StoredEventUtm**](StoredEventUtm.md) |  | [optional] 
**Zrn** | **string** | Ad ID from the &#x60;zrn&#x60; parameter Zernio adds to links of ads it creates. | [optional] 
**ClickIds** | [**StoredEventClickIds**](StoredEventClickIds.md) |  | [optional] 
**DestinationsSent** | **int** | Destinations the event was forwarded to. | [optional] 
**HasEmail** | **bool** |  | [optional] 
**HasPhone** | **bool** |  | [optional] 
**HasExternalId** | **bool** |  | [optional] 
**Ad** | [**StoredEventAd**](StoredEventAd.md) |  | [optional] 
**Deliveries** | [**List&lt;ListEvents200ResponseEventsInnerAllOfDeliveriesInner&gt;**](ListEvents200ResponseEventsInnerAllOfDeliveriesInner.md) | Each destination the event was forwarded to, with its latest send status. The full detail is on GET /v1/events/{eventId}. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

