# Zernio.Model.TargetingSpec
Normalized, platform-agnostic ad-targeting spec. Every field is optional, an empty object targets the platform's default broadest audience. Field names are camelCase and identical across `POST /v1/ads/create` (the `targeting` object), `POST /v1/ads/targeting/reach-estimate`, and `saved_targeting` audiences, so a spec resolved once can be reused verbatim.  Entity ids (`regions[].key`, `cities[].key`, `zips[].key`, `metros[].key`, `interests[].id`, `behaviors[].id`) are the platform's opaque identifiers resolved via `GET /v1/ads/targeting/search`. A spec is therefore meaningful only for the platform it was built against, except the portable fields (`countries`, `ageMin`/`ageMax`, `gender`, `incomeTier`, `languages`) which carry across platforms. Fields a platform cannot honour are rejected at create time with `INVALID_FIELD_VALUE` naming the offending field (not silently dropped). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Countries** | **List&lt;string&gt;** | ISO 3166-1 alpha-2 country codes (e.g. [&#39;US&#39;]). | [optional] 
**Regions** | [**List&lt;CreateStandaloneAdRequestZipsInner&gt;**](CreateStandaloneAdRequestZipsInner.md) | Region/state targeting. &#x60;key&#x60; is the platform location ID from /v1/ads/targeting/search?dimension&#x3D;geo&amp;geoType&#x3D;region. | [optional] 
**Cities** | [**List&lt;TargetingSpecCitiesInner&gt;**](TargetingSpecCitiesInner.md) | City targeting. Optional &#x60;radius&#x60; + &#x60;distanceUnit&#x60; extend beyond the city limits; both must be set together or both omitted. &#x60;radius&#x60; is only honoured on platforms whose capability map allows city radius (Meta). | [optional] 
**Zips** | [**List&lt;CreateStandaloneAdRequestZipsInner&gt;**](CreateStandaloneAdRequestZipsInner.md) | Postal/ZIP targeting. &#x60;key&#x60; is the platform&#39;s postal location ID (e.g. Meta &#x60;US:94304&#x60;). Supported on Meta, Google, TikTok, Pinterest, X. | [optional] 
**Metros** | [**List&lt;CreateStandaloneAdRequestZipsInner&gt;**](CreateStandaloneAdRequestZipsInner.md) | DMA / metro-area targeting. &#x60;key&#x60; is the platform&#39;s metro ID (e.g. Meta &#x60;DMA:807&#x60;). | [optional] 
**CustomLocations** | [**List&lt;TargetingSpecCustomLocationsInner&gt;**](TargetingSpecCustomLocationsInner.md) | Point-radius (lat/lng) targeting (Meta custom_locations / Google proximity). Honoured only where the capability map allows radius (Meta). | [optional] 
**ExcludedLocations** | [**TargetingSpecExcludedLocations**](TargetingSpecExcludedLocations.md) |  | [optional] 
**AgeMin** | **int** |  | [optional] 
**AgeMax** | **int** |  | [optional] 
**Gender** | **string** | Restrict by gender. &#39;all&#39; (default) targets everyone. | [optional] 
**IncomeTier** | **string** | Normalized household-income tier (ZIP/percentile based). Meta and TikTok express all four. Google maps only &#x60;top_10&#x60; (its INCOME_RANGE_90_UP); other tiers on Google, and any income tier on LinkedIn / X / Pinterest, are rejected. On Meta, income/zip targeting requires the relevant &#x60;specialAdCategories&#x60; to be unset (housing/employment/credit ads cannot use it).  | [optional] 
**Languages** | **List&lt;string&gt;** | Language codes (e.g. [&#39;en&#39;]). | [optional] 
**Interests** | [**List&lt;CreateStandaloneAdRequestBehaviorsInner&gt;**](CreateStandaloneAdRequestBehaviorsInner.md) | Interest entities from /v1/ads/targeting/search?dimension&#x3D;interest. Each carries the platform&#39;s opaque id. | [optional] 
**Behaviors** | [**List&lt;CreateStandaloneAdRequestBehaviorsInner&gt;**](CreateStandaloneAdRequestBehaviorsInner.md) | Behaviour entities from /v1/ads/targeting/search?dimension&#x3D;behavior. Supported on Meta and TikTok. | [optional] 
**Industries** | **List&lt;string&gt;** | LinkedIn B2B only. Industry URN id fragments. | [optional] 
**CompanySizes** | **List&lt;string&gt;** | LinkedIn B2B only. | [optional] 
**Seniorities** | **List&lt;string&gt;** | LinkedIn B2B only. | [optional] 
**JobFunctions** | **List&lt;string&gt;** | LinkedIn B2B only. | [optional] 
**AudienceInclude** | **List&lt;string&gt;** | Platform audience IDs to include. | [optional] 
**AudienceExclude** | **List&lt;string&gt;** | Platform audience IDs to exclude. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

