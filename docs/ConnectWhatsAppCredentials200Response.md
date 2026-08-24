# Zernio.Model.ConnectWhatsAppCredentials200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **string** |  | [optional] 
**RegistrationWarning** | **string** | Present when the account was created but Meta rejected the Cloud API registration. The number cannot send messages until this is resolved. | [optional] 
**WebhookNotice** | **string** | Present when the WABA webhook subscription (with the Zernio override callback) succeeded. Explains the delivery cutover and warns against unsubscribing the app from the WABA afterward. | [optional] 
**Account** | [**ConnectWhatsAppCredentials200ResponseAccount**](ConnectWhatsAppCredentials200ResponseAccount.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

