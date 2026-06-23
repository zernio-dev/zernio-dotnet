# Zernio.Model.ListBroadcastRecipients200ResponseRecipientsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**ContactId** | **string** |  | [optional] 
**ChannelId** | **string** |  | [optional] 
**PlatformIdentifier** | **string** |  | [optional] 
**ContactName** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**MessageId** | **string** |  | [optional] 
**Error** | **string** |  | [optional] 
**ErrorCode** | **int?** | Meta WhatsApp error code (e.g. 131049 for antispam, 131021 for invalid phone, 131026 for re-engagement required). Only populated for status&#x3D;failed. | [optional] 
**ErrorExplanation** | **string** | Plain-language translation of errorCode (e.g. for 131026, that the recipient has likely opted out of marketing messages). Null for unmapped codes; fall back to error. | [optional] 
**SentAt** | **DateTime** |  | [optional] 
**DeliveredAt** | **DateTime** |  | [optional] 
**ReadAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

