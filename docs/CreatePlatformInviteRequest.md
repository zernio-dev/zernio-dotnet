# Zernio.Model.CreatePlatformInviteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | The profile the account is connected to. | 
**Platform** | **string** |  | 
**AccountId** | **string** | Reconnect this existing account instead of adding a new one. It must belong to the profile and platform. | [optional] 
**LoginMethod** | **string** | Instagram only. instagram_login (the default) uses Instagram Login, facebook_login uses Facebook Login. A reconnect link keeps the method the account was connected with. | [optional] 
**ExpiresInDays** | **int** | Days until the link expires. | [optional] [default to 7]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

