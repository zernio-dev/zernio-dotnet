# Zernio.Model.CreateStandaloneAdRequestCitiesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** | Meta city ID, from /v1/ads/targeting/search results. | 
**Radius** | **decimal** | Optional radius around the city. Must be set together with distance_unit. Meta enforces a minimum city radius (~17 km / 10 mi); smaller values resolve to a 0-size audience and the ad fails at launch. For a tighter catchment use customLocations (lat/lng). | [optional] 
**DistanceUnit** | **string** | Unit for radius. Required if radius is set. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

