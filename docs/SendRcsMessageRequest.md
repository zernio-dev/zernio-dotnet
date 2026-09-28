# Zernio.Model.SendRcsMessageRequest
Send exactly one of text or content.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AgentId** | **string** |  | 
**To** | **string** | Recipient number (E.164; formatting is normalized). | 
**Text** | **string** |  | [optional] 
**Content** | [**RcsContent**](RcsContent.md) |  | [optional] 
**FallbackText** | **string** |  | [optional] 
**TtlSeconds** | **int** | Seconds before an undelivered message expires. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

