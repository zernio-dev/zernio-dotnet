# Zernio.Model.OrderImessageSenderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**Kind** | **string** |  | 
**Region** | **string** | Required for phone senders. Without availableNumberId the number is carrier-assigned in this region and revealed once the sender activates. | [optional] 
**AvailableNumberId** | **string** | A number from GET /v1/imessage/senders/available-numbers. It is assigned and activated on order instead of waiting for provisioning. Phone senders only. | [optional] 
**ZipCode** | **string** | US phone senders only. Preferred area for a carrier-assigned number (ignored with availableNumberId). | [optional] 
**EmailName** | **string** | Local part for email senders (required for kind: email) | [optional] 
**EmailDomain** | **string** | Domain for email senders (required for kind: email) | [optional] 
**DisplayName** | **string** |  | [optional] 
**PurchaseIntentId** | **string** | Idempotency key for safe retries | [optional] 
**Contact** | [**OrderImessageSenderRequestContact**](OrderImessageSenderRequestContact.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

