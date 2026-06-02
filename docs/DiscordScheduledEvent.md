# Zernio.Model.DiscordScheduledEvent
Discord guild scheduled event. Returned by /v1/discord/guilds/{guildId}/events endpoints. Fields below are the subset Zernio consumes — Discord may return more (e.g. creator, image hash) which we pass through verbatim. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Event snowflake ID | [optional] 
**GuildId** | **string** |  | [optional] 
**ChannelId** | **string** | Voice/stage channel ID; null for external events. | [optional] 
**CreatorId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**ScheduledStartTime** | **DateTime** |  | [optional] 
**ScheduledEndTime** | **DateTime** | Required for external events; optional for voice/stage. | [optional] 
**PrivacyLevel** | **int** | Always 2 (GUILD_ONLY) — Discord deprecated PUBLIC events. | [optional] 
**Status** | **int** | 1&#x3D;SCHEDULED, 2&#x3D;ACTIVE, 3&#x3D;COMPLETED, 4&#x3D;CANCELED | [optional] 
**EntityType** | **int** | 1&#x3D;STAGE_INSTANCE, 2&#x3D;VOICE, 3&#x3D;EXTERNAL | [optional] 
**EntityId** | **string** |  | [optional] 
**EntityMetadata** | [**DiscordScheduledEventEntityMetadata**](DiscordScheduledEventEntityMetadata.md) |  | [optional] 
**UserCount** | **int** | Number of members who RSVP&#39;d. Only present when withUserCount&#x3D;true on list. | [optional] 
**Image** | **string** | Cover image hash; build URL via cdn.discordapp.com. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

