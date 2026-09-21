# Zernio.Model.CreateImessageGroupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The iMessage account (sender) that opens the group | 
**Contacts** | **List&lt;string&gt;** | Participant handles (E.164 phones or iMessage emails) | 
**Text** | **string** | The first message | 
**Name** | **string** | Group name (required for WhatsApp groups) | [optional] 
**Channel** | **string** |  | [optional] [default to ChannelEnum.Imessage]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

