# Zernio.Model.SyncExternalPosts200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Synced** | [**SyncExternalPosts200ResponseSynced**](SyncExternalPosts200ResponseSynced.md) |  | [optional] 
**Found** | **bool** | Present only when a locator (&#x60;url&#x60;/&#x60;postId&#x60;) was provided — whether the post was found. | [optional] 
**Post** | [**ExternalPostSummary**](ExternalPostSummary.md) |  | [optional] 
**Posts** | [**List&lt;ExternalPostSummary&gt;**](ExternalPostSummary.md) | The account&#39;s recent external posts. Present only when no locator was provided. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

