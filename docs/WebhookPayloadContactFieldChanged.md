# Zernio.Model.WebhookPayloadContactFieldChanged

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Id** | **string** | Event id, the dedupe key. | 
**Event** | **string** |  | 
**Timestamp** | **DateTime** |  | 
**Contact** | [**WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**Field** | **string** | Custom field slug. | 
**PreviousValue** | **Object** |  | 
**Value** | **Object** |  | 
**Source** | **string** | Who wrote the field: the API or dashboard, a workflow set_field node, or an automation. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

