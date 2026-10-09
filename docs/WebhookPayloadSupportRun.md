# Zernio.Model.WebhookPayloadSupportRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Id** | **string** | Event id, the dedupe key. | 
**Event** | **string** |  | 
**Timestamp** | **DateTime** |  | 
**Run** | [**SupportRun**](SupportRun.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

