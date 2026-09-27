# Zernio.Model.WebhookPayloadTest
Webhook payload for test deliveries

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**Event** | **string** |  | 
**Message** | **string** | Human-readable test message | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this test event (set once when the payload is built). Test fires are sent synchronously as a single attempt; a later redelivery of this event keeps the original value. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

