# Zernio.Model.ConnectWechatCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AppId** | **string** | The Official Account&#39;s AppID (starts with wx). | 
**AppSecret** | **string** | The Official Account&#39;s AppSecret (32 characters). | 
**State** | **string** | Required state formatted as {userId}-{profileId}. Get userId from GET /v1/users and profileId from GET /v1/profiles. | 
**DisplayName** | **string** | Name to show for the account. Defaults to \&quot;WeChat Official Account\&quot;. | [optional] 
**RedirectUrl** | **string** | Optional URL to redirect to after a successful connection. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

