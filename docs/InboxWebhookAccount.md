# Zernio.Model.InboxWebhookAccount
The account context included in inbox webhook payloads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Social account ID | 
**AccountId** | **string** | Social account ID (same value as id). Canonical field so consumers can filter every webhook event on one field (e.g. route staging vs production by account). id is kept for backward compatibility. | [optional] 
**Platform** | **string** |  | 
**Username** | **string** |  | 
**DisplayName** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

