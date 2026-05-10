# Zernio.Model.XApiOperation
A single X API operation with its per-call price and the Zernio platform methods that trigger it.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Operation** | **string** | Internal operation key. Matches keys in &#x60;xApiCallsByOperation&#x60;. | [optional] 
**EventType** | **string** | Metronome &#x60;event_type&#x60; emitted when this operation runs. | [optional] 
**DisplayName** | **string** | Human-readable label shown on Metronome invoices. | [optional] 
**PricePerCallUsd** | **decimal** |  | [optional] 
**PricePerCallCents** | **decimal** | Per-call price in cents. Fractional values are intentional. | [optional] 
**Tier** | **string** | Tier key derived from &#x60;pricePerCallUsd&#x60; (e.g. &#x60;x_api_005&#x60; for $0.005, &#x60;x_api_200&#x60; for $0.200). Useful for grouping operations by price in dashboards.  | [optional] 
**TriggeredBy** | [**List&lt;XApiOperationTriggeredByInner&gt;**](XApiOperationTriggeredByInner.md) | Zernio platform methods that emit this operation, with their metering rule. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

