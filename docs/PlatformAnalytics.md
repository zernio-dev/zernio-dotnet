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
**ErrorMessage** | **string** | Failure detail:  - Failed entries: why the post failed to publish. - Unavailable entries: why analytics cannot be synced (e.g. Google Business Profile, a TikTok upload that never received a video id). - Pending entries: the most recent analytics sync error for the account (null while no sync has failed), cleared after the next successful sync. | [optional] 
**ErrorCode** | **string** | Stable machine-readable reason for errorMessage. New values may be added.  - post_not_found: the post was deleted or is no longer visible to the account. - not_post_owner: the post is owned by another Page or user (collab or visitor post); its analytics cannot be read with this Page&#39;s token. - permission_missing: the last analytics sync of the Facebook account failed because the Page no longer grants pages_read_engagement (pending entries only). - null: no stable code; read errorMessage. | [optional] 
**IsOwner** | **bool?** | Facebook only: true when the connected Page authored the post, false when Facebook reports another author (a collab post), null when unknown or for other platforms. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

