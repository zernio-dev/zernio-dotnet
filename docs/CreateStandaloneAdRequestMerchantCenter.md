# Zernio.Model.CreateStandaloneAdRequestMerchantCenter
Google Performance Max only; any other campaign type returns 400. Links the new campaign to a Merchant Center account. Google rejects the create, and nothing is created, when the ad account is not linked to that Merchant Center.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MerchantId** | **string** | Numeric Merchant Center id. | 
**FeedLabel** | **string** | Feed label to use. Omitted, every feed of the Merchant Center is used. | [optional] 
**ListingType** | **string** | Set to &#x60;vehicles&#x60; for vehicle listings. Omitted, the campaign is a retail Performance Max campaign. Vehicle ads require Google to allowlist the ad account; otherwise Google rejects the create. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

