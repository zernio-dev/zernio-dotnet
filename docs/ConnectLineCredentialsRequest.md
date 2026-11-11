# Zernio.Model.ConnectLineCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **string** | The Messaging API channel&#39;s Channel ID (digits only). | 
**ChannelSecret** | **string** | The Messaging API channel&#39;s Channel secret (32 hex characters). | 
**State** | **string** | Required state formatted as {userId}-{profileId}. Get userId from GET /v1/users and profileId from GET /v1/profiles. | 
**RedirectUrl** | **string** | Optional URL to redirect to after a successful connection. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

