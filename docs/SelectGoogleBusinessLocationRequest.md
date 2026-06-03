# Zernio.Model.SelectGoogleBusinessLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Profile ID from your connection flow | 
**LocationId** | **string** | The Google Business location ID selected by the user | 
**AccountId** | **string** | Optional but recommended. The Google Business Account resource name (\&quot;accounts/123\&quot;) that owns the selected location (returned per-location by GET /v1/connect/googlebusiness/locations). When provided, the location is resolved directly instead of by enumerating the account, which is required for accounts that own many locations. Omit only for small accounts.  | [optional] 
**PendingDataToken** | **string** | Token from the OAuth callback redirect (pendingDataToken query param). Tokens and profile data are retrieved server-side from this token. | 
**RedirectUrl** | **string** | Optional custom redirect URL to return to after selection | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

