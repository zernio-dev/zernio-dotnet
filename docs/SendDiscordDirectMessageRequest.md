# Zernio.Model.SendDiscordDirectMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | SocialAccount _id of the connected Discord account the bot speaks as. Caller must own the account (directly or via team membership). | 
**UserId** | **string** | Discord snowflake ID of the recipient (15-21 digits). | 
**Content** | **string** | Message text, up to 2,000 characters. | [optional] 
**Embeds** | **List&lt;Object&gt;** | Up to 10 Discord embeds. Same shape as channel-post embeds (title, description, color, fields, etc.). See DiscordPlatformData.embeds for the embed object schema. | [optional] 
**Attachments** | [**List&lt;SendDiscordDirectMessageRequestAttachmentsInner&gt;**](SendDiscordDirectMessageRequestAttachmentsInner.md) | Up to 10 media attachments. Each is &#x60;{ type: image|video|gif|document, url, filename?, mimeType?, size? }&#x60;. | [optional] 
**Tts** | **bool** | Send as text-to-speech message. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

