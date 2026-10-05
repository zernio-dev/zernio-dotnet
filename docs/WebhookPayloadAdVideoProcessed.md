# Zernio.Model.WebhookPayloadAdVideoProcessed
Webhook payload for the `ad.video.processed` event. Fires once per `POST /v1/ads/videos` call made with `async: true`, when Meta finishes processing the video (Meta only). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadAdVideoProcessedAccount**](WebhookPayloadAdVideoProcessedAccount.md) |  | 
**Video** | [**WebhookPayloadAdVideoProcessedVideo**](WebhookPayloadAdVideoProcessedVideo.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

