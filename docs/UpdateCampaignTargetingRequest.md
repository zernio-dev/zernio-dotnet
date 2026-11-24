# Zernio.Model.UpdateCampaignTargetingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to stage this change instead of applying it. Nothing is written to the ad network; the response is &#x60;202&#x60; with the staged change and its diff. Apply it with POST /v1/ads/changes/{changeId}/confirm. Cannot be combined with &#x60;validateOnly&#x60; or &#x60;dryRun&#x60;. | [optional] 
**Platform** | **string** |  | 
**Targeting** | [**UpdateCampaignTargetingRequestTargeting**](UpdateCampaignTargetingRequestTargeting.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

