# Zernio.Model.OAuthAppWebhook
Facebook and Instagram only: Meta delivers comments and messages to your app's own webhook, so set it to this callback URL and verify token on the app's webhook product (Page for Facebook, Instagram for Instagram) and subscribe the listed fields. Zernio checks each delivery against your app secret. Null on platforms with nothing to set up.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CallbackUrl** | **string** |  | 
**VerifyToken** | **string** |  | 
**Object** | **string** | The webhook object to configure. | 
**Fields** | **List&lt;string&gt;** | Subscribe the app to these fields. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

