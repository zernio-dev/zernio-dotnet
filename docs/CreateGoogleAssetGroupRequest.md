# Zernio.Model.CreateGoogleAssetGroupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Name** | **string** | Unique within the campaign. | 
**FinalUrls** | **List&lt;string&gt;** |  | 
**FinalMobileUrls** | **List&lt;string&gt;** |  | [optional] 
**Path1** | **string** |  | [optional] 
**Path2** | **string** | Requires path1. | [optional] 
**Status** | **string** |  | [optional] [default to StatusEnum.PAUSED]
**Assets** | [**List&lt;GoogleAssetGroupAssetLink&gt;**](GoogleAssetGroupAssetLink.md) |  | [optional] 
**ListingGroupFilter** | [**GoogleListingGroupTree**](GoogleListingGroupTree.md) |  | [optional] 
**ValidateOnly** | **bool** |  | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

