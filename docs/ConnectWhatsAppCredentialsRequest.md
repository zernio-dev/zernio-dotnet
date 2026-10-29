# Zernio.Model.ConnectWhatsAppCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Your Zernio profile ID | 
**AccessToken** | **string** | Permanent System User access token from Meta Business Suite | 
**WabaId** | **string** | WhatsApp Business Account ID from Meta | 
**PhoneNumberId** | **string** | Phone Number ID from Meta WhatsApp Manager | 
**Pin** | **string** | The 6-digit two-step verification PIN set on the number. Required if you enabled two-step verification for it, otherwise Meta rejects the Cloud API registration with error 133005 and the number cannot send messages. | [optional] 
**OauthAppId** | **string** | Your own WhatsApp OAuth app (see /v1/connect/oauth-apps) holding the Meta app the access token belongs to. The WABA&#39;s webhooks then go to that app&#39;s own callback URL and every delivery is checked against its app secret. Without it, deliveries come to Zernio&#39;s shared Meta webhook. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

