# Zernio.Model.WebhookPayloadAccountPermissionsChangedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**ProfileId** | **string** |  | 
**Platform** | **string** |  | 
**Username** | **string** |  | 
**DisplayName** | **string** |  | [optional] 
**OauthAppId** | **string** | The OAuth app the account connected through. | 
**MissingScopeAreas** | **List&lt;WebhookPayloadAccountPermissionsChangedAccount.MissingScopeAreasEnum&gt;** | Every area now missing. Enable the permission on your app (or have the user grant it), then reconnect the account. | 
**Reason** | **string** | The platform error that revealed it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

