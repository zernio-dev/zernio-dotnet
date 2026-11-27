# Zernio.Model.UpdateAdAudienceRequest
At least one field is required.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**Spec** | [**TargetingSpec**](TargetingSpec.md) | Full replacement for the stored targeting spec. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

