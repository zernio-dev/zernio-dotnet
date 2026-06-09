# Zernio.Model.WebhookLog
A single webhook delivery attempt recorded by Zernio (30-day retention).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserId** | **string** | ID of the account owner the webhook belongs to | [optional] 
**WebhookId** | **string** | ID of the webhook configuration that produced this delivery | [optional] 
**WebhookName** | **string** | Name of the webhook configuration at delivery time | [optional] 
**EventId** | **string** | Stable webhook event ID (correlates to the delivered payload) | [optional] 
**Event** | **string** | Event type that triggered the delivery (e.g. post.published) | [optional] 
**Url** | **string** | Destination URL the webhook was delivered to | [optional] 
**Status** | **string** | Delivery outcome | [optional] 
**StatusCode** | **int** | HTTP status code returned by the destination endpoint | [optional] 
**RequestPayload** | **Dictionary&lt;string, Object&gt;** | The JSON payload sent to the destination endpoint | [optional] 
**ResponseBody** | **string** | Response body returned by the destination endpoint | [optional] 
**ErrorMessage** | **string** | Error message when delivery failed | [optional] 
**AttemptNumber** | **int** | Delivery attempt number (increments on retries) | [optional] 
**ResponseTime** | **int** | Time taken by the destination endpoint to respond, in milliseconds | [optional] 
**CreatedAt** | **DateTime** | Timestamp the delivery was attempted | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

