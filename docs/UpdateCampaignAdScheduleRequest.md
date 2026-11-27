# Zernio.Model.UpdateCampaignAdScheduleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Schedule** | [**List&lt;UpdateCampaignAdScheduleRequestScheduleInner&gt;**](UpdateCampaignAdScheduleRequestScheduleInner.md) | The complete set of windows. Required, so clearing the schedule is always deliberate rather than an omission. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

