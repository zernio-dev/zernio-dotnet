# Zernio.Model.TargetingSpecCitiesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** |  | 
**Name** | **string** |  | [optional] 
**Radius** | **decimal** | Radius around the city. Requires distanceUnit. Meta enforces a minimum city radius (~17 km / 10 mi); smaller values resolve to a 0-size audience and the ad fails at launch. For a tighter catchment use customLocations (lat/lng), which allows a smaller radius. | [optional] 
**DistanceUnit** | **string** | Required if radius is set. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

