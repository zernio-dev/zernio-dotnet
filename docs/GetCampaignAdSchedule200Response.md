# Zernio.Model.GetCampaignAdSchedule200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CampaignId** | **string** |  | [optional] 
**Schedule** | [**List&lt;AdScheduleWindow&gt;**](AdScheduleWindow.md) |  | [optional] 
**ServesAroundTheClock** | **bool** | True when the campaign carries no ad schedule at all, so it can serve at any time. | [optional] 
**CachedAt** | **DateTime?** |  | [optional] 
**Stale** | **bool** | True when a quota-exhausted read served the last-good copy. | [optional] 
**Performance** | [**GetCampaignAdSchedule200ResponsePerformance**](GetCampaignAdSchedule200ResponsePerformance.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

