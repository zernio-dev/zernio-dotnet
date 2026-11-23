# Zernio.Model.ConnectTradeDeskAdsPartnerRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PartnerId** | **string** | Trade Desk Partner ID, a short code such as &#x60;ptn1234&#x60;. Stored and echoed lowercased. | 
**ApiToken** | **string** | API token of a Trade Desk user with API access to the partner. | 
**AdAccountIds** | **List&lt;string&gt;** | Advertiser ids to keep. Left out or empty, a new connection keeps every advertiser and a reconnect keeps its saved selection. | [optional] 
**Name** | **string** | Optional display name for the account. | [optional] 
**ProfileId** | **string** | Your Zernio profile ID | 
**State** | **string** | Optional state passthrough for the connect flow. | [optional] 
**RedirectUrl** | **string** | Optional URL to redirect to after a successful connection, echoed back as redirectUrl. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

