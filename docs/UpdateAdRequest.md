# Zernio.Model.UpdateAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Headlines** | [**List&lt;GoogleRsaHeadline&gt;**](GoogleRsaHeadline.md) | Google RSA only. Replaces the complete headline list. No padding or truncation on update. | [optional] 
**Descriptions** | [**List&lt;GoogleRsaDescription&gt;**](GoogleRsaDescription.md) | Google RSA only. Replaces the complete description list. No padding or truncation on update. | [optional] 
**FinalUrls** | **List&lt;string&gt;** | Google RSA only. Replaces final URLs. Omitted lists stay unchanged. | [optional] 
**Status** | **string** |  | [optional] 
**Budget** | [**UpdateAdRequestBudget**](UpdateAdRequestBudget.md) |  | [optional] 
**Targeting** | [**UpdateAdRequestTargeting**](UpdateAdRequestTargeting.md) |  | [optional] 
**Creative** | [**UpdateAdRequestCreative**](UpdateAdRequestCreative.md) |  | [optional] 
**Name** | **string** | Rename the ad. Now propagated to Meta (POST /{ad-id}); non-Meta platforms return 501. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

