# Zernio.Model.UpdateCampaignConversionGoalsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Goals** | [**List&lt;GoogleBiddableGoalInput&gt;**](GoogleBiddableGoalInput.md) |  | [optional] 
**GoalConfigLevel** | **string** |  | [optional] 
**CustomConversionGoalId** | **string** | Custom goal to bid on, or null to clear | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

