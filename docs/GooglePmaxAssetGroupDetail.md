# Zernio.Model.GooglePmaxAssetGroupDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable Google asset group id. Use it in the asset-group endpoints below. | 
**ResourceName** | **string** | customers/{customerId}/assetGroups/{assetGroupId} | 
**CampaignId** | **string** |  | 
**Name** | **string** |  | 
**Status** | **string** | Asset-group status on Google. Campaign status independently controls delivery. | 
**FinalUrls** | **List&lt;string&gt;** |  | 
**FinalMobileUrls** | **List&lt;string&gt;** |  | 
**Path1** | **string** |  | 
**Path2** | **string** |  | 
**AdStrength** | **string** | Google ad strength, such as POOR, AVERAGE, GOOD or EXCELLENT. | 
**PrimaryStatus** | **string** | Why the group is or is not serving, such as ELIGIBLE, PAUSED or NOT_ELIGIBLE. | 
**PrimaryStatusReasons** | **List&lt;string&gt;** |  | 
**Assets** | [**List&lt;GooglePmaxAssetGroupAssetsInner&gt;**](GooglePmaxAssetGroupAssetsInner.md) |  | 
**ListingGroupFilters** | [**List&lt;GoogleListingGroupFilterNode&gt;**](GoogleListingGroupFilterNode.md) | The asset group&#39;s listing-group tree as flat nodes (retail campaigns). Empty when the group has none. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

