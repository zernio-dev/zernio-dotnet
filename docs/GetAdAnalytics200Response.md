# Zernio.Model.GetAdAnalytics200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ad** | [**GetAdAnalytics200ResponseAd**](GetAdAnalytics200ResponseAd.md) |  | [optional] 
**BackfillPending** | **bool** | Present and true only on &#x60;202&#x60; responses: part of the requested date range is still being backfilled from the platform in the background. Retry the same request shortly; it returns 200 once the range is fully ingested. | [optional] 
**Analytics** | [**GetCampaignAnalytics200ResponseAnalytics**](GetCampaignAnalytics200ResponseAnalytics.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

