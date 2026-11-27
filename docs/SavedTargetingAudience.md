# Zernio.Model.SavedTargetingAudience
A reusable, stored TargetingSpec. No member upload step, no adAccountId, the spec is the audience. Reference it later via `savedTargetingId` on POST /v1/ads/create.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Type** | **string** |  | 
**AccountId** | **string** | Account ID on the target ad platform. | 
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Spec** | [**TargetingSpec**](TargetingSpec.md) | The targeting spec to store. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

