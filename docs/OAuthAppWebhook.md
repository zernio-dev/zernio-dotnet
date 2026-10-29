# Zernio.Model.OAuthAppWebhook
Facebook and Instagram only; null on platforms with nothing to set up. Meta delivers comments and messages to your app's own webhook.  Set this callback URL and verify token on the app's webhook product (Page for Facebook, Instagram for Instagram) and subscribe the listed fields. Zernio checks each delivery against your app secret. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CallbackUrl** | **string** |  | 
**VerifyToken** | **string** |  | 
**Object** | **OAuthAppWebhookObject** |  | 
**Fields** | **List&lt;string&gt;** | Subscribe the app to these fields. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

