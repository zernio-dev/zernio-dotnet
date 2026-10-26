# Zernio.Model.SendEventsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Profile the events belong to. Its saved destinations receive the events. | 
**Events** | [**List&lt;ConversionEvent&gt;**](ConversionEvent.md) |  | 
**Destinations** | [**List&lt;SendEventsRequestDestinationsInner&gt;**](SendEventsRequestDestinationsInner.md) | Send to these destinations instead of the saved ones (every event goes to each). | [optional] 
**Consent** | [**SendEventsRequestConsent**](SendEventsRequestConsent.md) |  | [optional] 
**TestCode** | **string** | Forwarded as each platform test code (see POST /v1/ads/conversions). Test events are not stored. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

