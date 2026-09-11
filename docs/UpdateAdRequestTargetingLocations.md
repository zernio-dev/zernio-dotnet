# Zernio.Model.UpdateAdRequestTargetingLocations
Google and LinkedIn. The FULL new location set for the campaign. Bare country-code array, or an object with countries/regions/cities/zips/metros key lists (`key` from GET /v1/ads/targeting/search?dimension=geo). Equivalent to the top-level geo fields; sending both returns 400. Empty returns 400, `customLocations` returns 422.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Countries** | **List&lt;string&gt;** |  | [optional] 
**Regions** | [**List&lt;UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner&gt;**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner.md) |  | [optional] 
**Cities** | [**List&lt;UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner&gt;**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner.md) |  | [optional] 
**Zips** | [**List&lt;UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner&gt;**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner.md) |  | [optional] 
**Metros** | [**List&lt;UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner&gt;**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

