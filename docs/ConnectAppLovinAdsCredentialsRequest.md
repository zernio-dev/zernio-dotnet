# Zernio.Model.ConnectAppLovinAdsCredentialsRequest
Send apiKey with eventKey, campaignApiKey with accountId, or all four. Each pair goes together (400 otherwise).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ApiKey** | **string** | Conversion API key from the Keys page of AppLovin Axon Ads Manager. Sent with eventKey. | [optional] 
**EventKey** | **string** | Event Key from the Keys page of AppLovin Axon Ads Manager: 8 to 128 letters, digits, dots, dashes or underscores. Sent with apiKey. | [optional] 
**CampaignApiKey** | **string** | Campaign Management API key from the Keys page of ads.axon.ai (visible to account Admins only). Sent with accountId. Lets Zernio read, create and manage campaigns and creative sets. | [optional] 
**AccountId** | **string** | Numeric AppLovin account id (Account menu, then Go to settings, in ads.axon.ai). Sent with campaignApiKey. | [optional] 
**ReconnectAccountId** | **string** | The Zernio id of the AppLovin connection being reconnected (a connection on this profile). The keys sent update that connection, which keeps its identity, instead of creating one: send it to add or replace keys on an existing connection. | [optional] 
**ReportKey** | **string** | Optional Report Key from the Keys page of your AppLovin account. With it, Zernio syncs AppLovin spend per campaign. | [optional] 
**Name** | **string** | Optional display name for the account. | [optional] 
**ProfileId** | **string** | Your Zernio profile ID | 
**State** | **string** | Optional state passthrough for the connect flow. | [optional] 
**RedirectUrl** | **string** | Optional URL to redirect to after a successful connection, echoed back as redirectUrl. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

