# Zernio.Model.ImessageSenderLifecycle
A provisioned iMessage sender order and its lifecycle. Activation is asynchronous: poll GET /v1/imessage/senders/{senderId} or subscribe to account.connected.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Kind** | **string** |  | [optional] 
**Region** | **string** |  | [optional] 
**Handle** | **string** | The sender handle once activation assigns it | [optional] 
**OptInLink** | **string** | imessage:// deep link that opens Messages on this sender with a prefilled text. Share it so contacts message you first (Apple only lets a sender reach contacts who wrote to it first); null until the handle is assigned. | [optional] 
**Status** | **string** |  | [optional] 
**PriceCents** | **int** | Monthly price billed while the sender is active | [optional] 
**Provider** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**FailureReason** | **string** |  | [optional] 
**AccountId** | **string** | The messaging account created at activation | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

