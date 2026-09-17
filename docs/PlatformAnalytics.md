# Zernio.Model.PlatformAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**PlatformPostId** | **string** | The native post ID on the platform (e.g. Instagram media ID, tweet ID) | [optional] 
**AccountId** | **string** |  | [optional] 
**AccountUsername** | **string** |  | [optional] 
**Analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] 
**SyncStatus** | **string** | Sync state of analytics for this platform | [optional] 
**PlatformPostUrl** | **string** |  | [optional] 
**ErrorMessage** | **string** | Failure detail. On failed entries, why the post failed to publish. On unavailable entries, why analytics cannot be synced (e.g. Google Business Profile, a TikTok upload that never received a video id). On pending entries, the most recent analytics sync error for the account (null while no sync has failed), cleared after the next successful sync. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

