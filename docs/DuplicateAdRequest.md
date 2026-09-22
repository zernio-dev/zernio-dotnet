# Zernio.Model.DuplicateAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdSetId** | **string** | Destination platform ad set id (defaults to the source&#39;s ad set) | [optional] 
**StatusOption** | **string** |  | [optional] [default to StatusOptionEnum.PAUSED]
**RenameStrategy** | **string** |  | [optional] 
**RenamePrefix** | **string** |  | [optional] 
**RenameSuffix** | **string** |  | [optional] 
**SyncAfter** | **bool** |  | [optional] [default to true]
**ReuseSourceCreative** | **bool** | Point the copy at the source ad&#39;s creative object instead of copying it, so the copy keeps the same Facebook post, the same Instagram media, their existing likes, comments and shares, and the full creative setup (text variations included). This is what Ads Manager&#39;s \&quot;show existing reactions, comments and shares\&quot; does. Meta&#39;s native copy always publishes new posts. A creative belongs to one ad account, so &#x60;adSetId&#x60; must be in the source ad&#39;s account. 400 when the source ad has no creative yet. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

