# Zernio.Model.ConnectBlueskyCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Identifier** | **string** | Your Bluesky handle (e.g. user.bsky.social) or email address | 
**AppPassword** | **string** | App password generated from Bluesky Settings &gt; App Passwords | 
**State** | **string** | Required state formatted as {userId}-{profileId}. Get userId from GET /v1/users and profileId from GET /v1/profiles. | 
**RedirectUrl** | **string** | Optional URL to redirect to after successful connection. Used when the state carries no redirect (a state minted by GET /v1/connect/bluesky with redirect_url already carries one, and that one wins). | [optional] 
**RedirectUri** | **string** | Alias of redirect_url, kept for existing callers | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

