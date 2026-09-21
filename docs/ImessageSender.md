# Zernio.Model.ImessageSender
An iMessage sender registered as an account on a profile.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Account id (use it with the inbox endpoints&#39; accountId) | [optional] 
**Platform** | **string** |  | [optional] 
**Sender** | **string** | The sender handle (E.164 phone or email) | [optional] 
**OptInLink** | **string** | imessage:// deep link that opens Messages on this sender with a prefilled text. Share it so contacts message you first (Apple only lets a sender reach contacts who wrote to it first). | [optional] 
**DisplayName** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**Provider** | **string** | Delivery provider backing this sender (e.g. loopmessage) | [optional] 
**SenderVerified** | **bool** | Whether the provider confirmed the sender as active at registration time | [optional] 
**IsActive** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

