# Zernio.Model.TikTokPlatformDataMusicSoundInfo
Commercial Music Library track to attach. Accounts connected through the TikTok for Business app only: a developer-app account rejects the post at publish time with a message that says so. Pick musicSoundId from GET /v1/accounts/{accountId}/tiktok/commercial-music. Ignored on drafts, where TikTok ignores every post_info field.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MusicSoundId** | **string** | The commercial_music_id of the track. | 
**MusicSoundVolume** | **int** | Track volume. TikTok defaults an omitted volume to 0, which publishes the track silently, so we default to the app&#39;s 50. Video posts only. | [optional] [default to 50]
**MusicSoundStart** | **int** | Start point of the track in milliseconds (default 0). Video posts only. | [optional] 
**MusicSoundEnd** | **int** | End point of the track in milliseconds (default: the video length). Must be greater than musicSoundStart. Video posts only. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

