# Zernio.Model.UpdateAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Headlines** | [**List&lt;GoogleRsaHeadline&gt;**](GoogleRsaHeadline.md) | Google Search and Display only. Replaces the complete headline list. Search takes 3-15, Display 1-5 and rejects pinnedField; the count is checked once the ad&#39;s channel is known. No padding or truncation on update. | [optional] 
**Descriptions** | [**List&lt;GoogleRsaDescription&gt;**](GoogleRsaDescription.md) | Google Search and Display only. Replaces the complete description list. Search takes 2-4, Display 1-5 and rejects pinnedField. No padding or truncation on update. | [optional] 
**FinalUrls** | **List&lt;string&gt;** | Google Search and Display only. Replaces final URLs. Omitted lists stay unchanged. For Performance Max use assetGroup.finalUrl. | [optional] 
**AssetGroup** | [**GooglePmaxAssetGroupUpdate**](GooglePmaxAssetGroupUpdate.md) | Google Performance Max only. Replaces whole asset roles on the ad&#39;s asset group. Returns 422 on any other platform or channel. | [optional] 
**Status** | **string** |  | [optional] 
**Budget** | [**UpdateAdRequestBudget**](UpdateAdRequestBudget.md) |  | [optional] 
**Targeting** | [**UpdateAdRequestTargeting**](UpdateAdRequestTargeting.md) |  | [optional] 
**Creative** | [**UpdateAdRequestCreative**](UpdateAdRequestCreative.md) |  | [optional] 
**Name** | **string** | Rename the ad. Now propagated to Meta (POST /{ad-id}); non-Meta platforms return 501. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

