# Zernio.Model.UpdateAdSetRequestPlacements
Meta only (400 elsewhere). Manual placements, with the same object and enums as `placements` on POST /v1/ads/create.  - **Object:** REPLACES the ad set's current placement set (`publisher_platforms`, every `*_positions` list and `device_platforms`). A position list you leave out is removed. An object with no non-empty list is a 400 (send `null` instead). - **`null`:** removes every placement key, so Meta returns to automatic (Advantage+) placements. - **Omitted:** placements are left untouched.  Meta enforces co-selection rules (e.g. a position needs its publisher platform) and its error is returned as is. Meta may also reject `null` or a narrower set when an ad's creative uses per-placement asset customization (`placementAssets`).  Cannot be combined with `targeting.placements` (400). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PublisherPlatforms** | **List&lt;UpdateAdSetRequestPlacements.PublisherPlatformsEnum&gt;** |  | [optional] 
**FacebookPositions** | **List&lt;UpdateAdSetRequestPlacements.FacebookPositionsEnum&gt;** |  | [optional] 
**InstagramPositions** | **List&lt;UpdateAdSetRequestPlacements.InstagramPositionsEnum&gt;** |  | [optional] 
**MessengerPositions** | **List&lt;UpdateAdSetRequestPlacements.MessengerPositionsEnum&gt;** |  | [optional] 
**AudienceNetworkPositions** | **List&lt;UpdateAdSetRequestPlacements.AudienceNetworkPositionsEnum&gt;** |  | [optional] 
**ThreadsPositions** | **List&lt;UpdateAdSetRequestPlacements.ThreadsPositionsEnum&gt;** |  | [optional] 
**WhatsappPositions** | **List&lt;UpdateAdSetRequestPlacements.WhatsappPositionsEnum&gt;** |  | [optional] 
**DevicePlatforms** | **List&lt;UpdateAdSetRequestPlacements.DevicePlatformsEnum&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

