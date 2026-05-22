# Zernio.Model.SavedTargetingAudience
A reusable, stored TargetingSpec. No member upload step, no adAccountId, the spec is the audience. Reference it later via `savedTargetingId` on POST /v1/ads/create.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**AccountId** | **string** | Social account ID on the target ad platform. | 
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Spec** | [**TargetingSpec**](TargetingSpec.md) | The targeting spec to store. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

