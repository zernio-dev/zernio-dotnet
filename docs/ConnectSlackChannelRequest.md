# Zernio.Model.ConnectSlackChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**ChannelId** | **string** | Slack channel id, C... or G... | 
**PendingDataToken** | **string** | Nonce from the OAuth redirect. Required unless accountId is sent. | [optional] 
**AccountId** | **string** | Existing Slack account whose workspace token is reused. Required unless pendingDataToken is sent. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

