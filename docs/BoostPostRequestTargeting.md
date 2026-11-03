# Zernio.Model.BoostPostRequestTargeting
Same geo/demographic fields as the `TargetingSpec` used by /v1/ads/create. Geo keys (`regions`/`cities`/`zips`/`metros`) resolve via GET /v1/ads/targeting/search?dimension=geo.  - Meta only: city radius and lat/lng `customLocations`. They preserve the boosted post's social proof (the ad references the existing post). - Reddit: the whole `TargetingSpec` applies, including `communities`, `excludedCommunities`, `conversationKeywords`, `excludedConversationKeywords`, `interests`, `audienceInclude` / `audienceExclude` and `excludedLocations`. Without any geo the ad targets the US. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AgeMin** | **int** |  | [optional] 
**AgeMax** | **int** |  | [optional] 
**Gender** | **string** | Applied on Meta, TikTok, Pinterest and Reddit. Ignored on Google, LinkedIn and X. | [optional] 
**Languages** | **List&lt;string&gt;** | Language codes, the same format as &#x60;languages&#x60; on POST /v1/ads/create.  - Meta: ISO 639-1 codes. A bare code targets all regional variants (\&quot;en\&quot; &#x3D; all English); use a region-qualified code for a specific one (\&quot;en_GB\&quot;, \&quot;pt_BR\&quot;). Meta numeric locale ids (e.g. \&quot;24\&quot; for English UK) are also accepted. Unknown values are rejected. - Reddit: ISO 639-1 codes (e.g. &#x60;en&#x60;). | [optional] 
**Countries** | **List&lt;string&gt;** | ISO country codes. Required for TikTok boosts (TikTok&#39;s ad group requires location_ids); optional on other platforms. | [optional] 
**Regions** | [**List&lt;UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf&gt;**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf.md) | Region/state targeting. &#x60;key&#x60; from /v1/ads/targeting/search?dimension&#x3D;geo&amp;geoType&#x3D;region. | [optional] 
**Cities** | [**List&lt;BoostPostRequestTargetingCitiesInner&gt;**](BoostPostRequestTargetingCitiesInner.md) | City targeting. Optional &#x60;radius&#x60; + &#x60;distanceUnit&#x60; extend beyond the city limits (both set together, Meta only). | [optional] 
**Zips** | [**List&lt;UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf&gt;**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf.md) | Postal/ZIP targeting. &#x60;key&#x60; is the platform&#39;s postal location ID (e.g. Meta &#x60;US:94304&#x60;). | [optional] 
**Metros** | [**List&lt;UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf&gt;**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf.md) | DMA / metro-area targeting. &#x60;key&#x60; is the platform&#39;s metro ID (e.g. Meta &#x60;DMA:807&#x60;). | [optional] 
**CustomLocations** | [**List&lt;BoostPostRequestTargetingCustomLocationsInner&gt;**](BoostPostRequestTargetingCustomLocationsInner.md) | Point-radius (lat/lng) targeting (Meta custom_locations). No geo &#x60;key&#x60; lookup needed. | [optional] 
**Interests** | [**List&lt;UpdateAdRequestTargetingInterestsInner&gt;**](UpdateAdRequestTargetingInterestsInner.md) | Interest objects from /v1/ads/interests. Each must include id and name. | [optional] 
**AdvantageAudience** | **int** | Meta only. 0 &#x3D; disabled (default), 1 &#x3D; enabled. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

