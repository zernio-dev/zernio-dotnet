# Zernio.Model.SelectPinterestBoardRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Your Zernio profile ID | 
**BoardId** | **string** | The Pinterest Board ID selected by the user | 
**BoardName** | **string** | The board name (for display purposes) | [optional] 
**TempToken** | **string** | Temporary Pinterest access token from OAuth | 
**UserProfile** | **Object** | User profile data from OAuth redirect | [optional] 
**RefreshToken** | **string** | Pinterest refresh token (if available) | [optional] 
**ExpiresIn** | **int** | Token expiration time in seconds | [optional] 
**RedirectUrl** | **string** | Custom redirect URL after connection completes | [optional] 
**OauthAppId** | **string** | The &#x60;oauthAppId&#x60; from the selection redirect, when the connect ran on one of your own OAuth apps. Pass it back so a retried selection stays on that app; a different app than the connect used returns 400. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

