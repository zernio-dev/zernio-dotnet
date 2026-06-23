# Zernio.Model.CreateStandaloneAdRequestPlacements
Meta only. Manual ad placements. Omit for automatic placements (Meta's default, recommended for most cases — Meta optimises delivery across all eligible surfaces). When set, restricts delivery to the chosen surfaces, mapped onto the ad set's `targeting.{publisher_platforms, facebook_positions, instagram_positions, messenger_positions, audience_network_positions, threads_positions, whatsapp_positions, device_platforms}`. Enum membership is validated here; Meta additionally enforces co-selection rules (e.g. some positions require their parent publisher platform) and returns an actionable error which we surface. Non-Meta platforms reject this field. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PublisherPlatforms** | **List&lt;CreateStandaloneAdRequestPlacements.PublisherPlatformsEnum&gt;** | Top-level platforms to deliver on. A position field below is only honoured when its parent platform is included here. | [optional] 
**FacebookPositions** | **List&lt;CreateStandaloneAdRequestPlacements.FacebookPositionsEnum&gt;** |  | [optional] 
**InstagramPositions** | **List&lt;CreateStandaloneAdRequestPlacements.InstagramPositionsEnum&gt;** |  | [optional] 
**MessengerPositions** | **List&lt;CreateStandaloneAdRequestPlacements.MessengerPositionsEnum&gt;** |  | [optional] 
**AudienceNetworkPositions** | **List&lt;CreateStandaloneAdRequestPlacements.AudienceNetworkPositionsEnum&gt;** |  | [optional] 
**ThreadsPositions** | **List&lt;CreateStandaloneAdRequestPlacements.ThreadsPositionsEnum&gt;** |  | [optional] 
**WhatsappPositions** | **List&lt;CreateStandaloneAdRequestPlacements.WhatsappPositionsEnum&gt;** |  | [optional] 
**DevicePlatforms** | **List&lt;CreateStandaloneAdRequestPlacements.DevicePlatformsEnum&gt;** | Restrict by device. Omit to deliver on both mobile and desktop. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

