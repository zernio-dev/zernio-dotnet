# Zernio.Model.SyncExternalPosts200ResponseSynced

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PostsFound** | **int** | Posts returned by the platform listing during the on-demand sync | [optional] 
**PostsSynced** | **int** | Stored records this call wrote: new posts and posts whose metadata changed. On LinkedIn personal profiles and the X fallback sync, posts whose metrics were refreshed are counted too. | [optional] 
**Skipped** | **bool** | True when the account was synced within the debounce window and no live fetch ran. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

