# Zernio.Model.ConnectWordPressWithApplicationPasswordRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Your Zernio profile ID (get from /v1/profiles). | 
**SiteUrl** | **string** | HTTPS base URL of the WordPress installation, including a subdirectory path when applicable. | 
**Username** | **string** | WordPress login name. A colon is not allowed. | 
**ApplicationPassword** | **string** | Application password created for the WordPress user. Spaces in WordPress display formatting are accepted. | 
**ReconnectAccountId** | **string** | The WordPress site connection being reconnected. In a workspace with no billing set up, the connect is allowed only when it returns to that same site. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

