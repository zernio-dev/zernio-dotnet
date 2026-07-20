# Zernio.Model.CtwaAdRequestBodyPlacements
Manual ad placements on the shared ad set. Omit for automatic placements. When set, restricts delivery to the chosen surfaces, mapped onto the ad set's `targeting.{publisher_platforms, facebook_positions, instagram_positions, messenger_positions, audience_network_positions, threads_positions, whatsapp_positions, device_platforms}`. Enum membership is validated here; Meta additionally enforces co-selection rules and restricts which placements are eligible for click-to-WhatsApp ads, returning an actionable error which we surface. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PublisherPlatforms** | **List&lt;CtwaAdRequestBodyPlacements.PublisherPlatformsEnum&gt;** | Top-level platforms to deliver on. A position field below is only honoured when its parent platform is included here. | [optional] 
**FacebookPositions** | **List&lt;CtwaAdRequestBodyPlacements.FacebookPositionsEnum&gt;** |  | [optional] 
**InstagramPositions** | **List&lt;CtwaAdRequestBodyPlacements.InstagramPositionsEnum&gt;** |  | [optional] 
**MessengerPositions** | **List&lt;CtwaAdRequestBodyPlacements.MessengerPositionsEnum&gt;** |  | [optional] 
**AudienceNetworkPositions** | **List&lt;CtwaAdRequestBodyPlacements.AudienceNetworkPositionsEnum&gt;** |  | [optional] 
**ThreadsPositions** | **List&lt;CtwaAdRequestBodyPlacements.ThreadsPositionsEnum&gt;** |  | [optional] 
**WhatsappPositions** | **List&lt;CtwaAdRequestBodyPlacements.WhatsappPositionsEnum&gt;** |  | [optional] 
**DevicePlatforms** | **List&lt;CtwaAdRequestBodyPlacements.DevicePlatformsEnum&gt;** | Restrict by device. Omit to deliver on both mobile and desktop. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

