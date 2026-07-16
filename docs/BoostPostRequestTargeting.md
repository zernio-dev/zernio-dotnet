# Zernio.Model.BoostPostRequestTargeting
Same geo/demographic fields as the `TargetingSpec` used by /v1/ads/create. Geo keys (`regions`/`cities`/`zips`/`metros`) resolve via GET /v1/ads/targeting/search?dimension=geo. City radius and lat/lng `customLocations` are Meta-only and preserve the boosted post's social proof (the ad references the existing post). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AgeMin** | **int** |  | [optional] 
**AgeMax** | **int** |  | [optional] 
**Gender** | **string** | Meta only. | [optional] 
**Languages** | **List&lt;string&gt;** | Meta locale ids (numeric), passed through as given. | [optional] 
**Countries** | **List&lt;string&gt;** | ISO country codes. Required for TikTok boosts (TikTok&#39;s ad group requires location_ids); optional on other platforms. | [optional] 
**Regions** | [**List&lt;BoostPostRequestTargetingRegionsInner&gt;**](BoostPostRequestTargetingRegionsInner.md) | Region/state targeting. &#x60;key&#x60; from /v1/ads/targeting/search?dimension&#x3D;geo&amp;geoType&#x3D;region. | [optional] 
**Cities** | [**List&lt;BoostPostRequestTargetingCitiesInner&gt;**](BoostPostRequestTargetingCitiesInner.md) | City targeting. Optional &#x60;radius&#x60; + &#x60;distanceUnit&#x60; extend beyond the city limits (both set together, Meta only). | [optional] 
**Zips** | [**List&lt;BoostPostRequestTargetingRegionsInner&gt;**](BoostPostRequestTargetingRegionsInner.md) | Postal/ZIP targeting. &#x60;key&#x60; is the platform&#39;s postal location ID (e.g. Meta &#x60;US:94304&#x60;). | [optional] 
**Metros** | [**List&lt;BoostPostRequestTargetingRegionsInner&gt;**](BoostPostRequestTargetingRegionsInner.md) | DMA / metro-area targeting. &#x60;key&#x60; is the platform&#39;s metro ID (e.g. Meta &#x60;DMA:807&#x60;). | [optional] 
**CustomLocations** | [**List&lt;BoostPostRequestTargetingCustomLocationsInner&gt;**](BoostPostRequestTargetingCustomLocationsInner.md) | Point-radius (lat/lng) targeting (Meta custom_locations). No geo &#x60;key&#x60; lookup needed. | [optional] 
**Interests** | [**List&lt;UpdateAdRequestTargetingInterestsInner&gt;**](UpdateAdRequestTargetingInterestsInner.md) | Interest objects from /v1/ads/interests. Each must include id and name. | [optional] 
**AdvantageAudience** | **int** | Meta only. 0 &#x3D; disabled (default), 1 &#x3D; enabled. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

