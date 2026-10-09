# Zernio.Model.WebhookPayloadContactTag

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Id** | **string** | Event id, the dedupe key. | 
**Event** | **string** |  | 
**Timestamp** | **DateTime** |  | 
**Contact** | [**WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**Tag** | **string** |  | 
**Source** | **string** | Who wrote the tag: the API or dashboard, a workflow add_tag / remove_tag node, or a comment-automation link click. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

