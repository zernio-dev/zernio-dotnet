# Zernio.Model.GoogleAssetUpdate
Supply fields for exactly one asset type per update. finalUrls may accompany sitelinkAsset. Shared asset edits affect every attachment using the asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssetResourceName** | **string** | Asset resource name returned by a list operation. Must belong to the selected customer. | 
**SitelinkAsset** | [**UpdateAccountSitelinksRequestUpdatesInnerSitelinkAsset**](UpdateAccountSitelinksRequestUpdatesInnerSitelinkAsset.md) |  | [optional] 
**FinalUrls** | **List&lt;string&gt;** |  | [optional] 
**CalloutAsset** | [**UpdateAccountCalloutsRequestUpdatesInnerCalloutAsset**](UpdateAccountCalloutsRequestUpdatesInnerCalloutAsset.md) |  | [optional] 
**StructuredSnippetAsset** | [**GoogleStructuredSnippet**](GoogleStructuredSnippet.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

