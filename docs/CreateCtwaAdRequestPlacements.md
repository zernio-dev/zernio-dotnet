# Zernio.Model.CreateCtwaAdRequestPlacements
Manual ad placements on the shared ad set. Omit for automatic placements. When set, restricts delivery to the chosen surfaces, mapped onto the ad set's `targeting.{publisher_platforms, facebook_positions, instagram_positions, messenger_positions, audience_network_positions, threads_positions, whatsapp_positions, device_platforms}`. Enum membership is validated here; Meta additionally enforces co-selection rules and restricts which placements are eligible for click-to-WhatsApp ads, returning an actionable error which we surface. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PublisherPlatforms** | **List&lt;CreateCtwaAdRequestPlacements.PublisherPlatformsEnum&gt;** | Top-level platforms to deliver on. A position field below is only honoured when its parent platform is included here. | [optional] 
**FacebookPositions** | **List&lt;CreateCtwaAdRequestPlacements.FacebookPositionsEnum&gt;** |  | [optional] 
**InstagramPositions** | **List&lt;CreateCtwaAdRequestPlacements.InstagramPositionsEnum&gt;** |  | [optional] 
**MessengerPositions** | **List&lt;CreateCtwaAdRequestPlacements.MessengerPositionsEnum&gt;** |  | [optional] 
**AudienceNetworkPositions** | **List&lt;CreateCtwaAdRequestPlacements.AudienceNetworkPositionsEnum&gt;** |  | [optional] 
**ThreadsPositions** | **List&lt;CreateCtwaAdRequestPlacements.ThreadsPositionsEnum&gt;** |  | [optional] 
**WhatsappPositions** | **List&lt;CreateCtwaAdRequestPlacements.WhatsappPositionsEnum&gt;** |  | [optional] 
**DevicePlatforms** | **List&lt;CreateCtwaAdRequestPlacements.DevicePlatformsEnum&gt;** | Restrict by device. Omit to deliver on both mobile and desktop. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

