# Zernio.Model.UpdateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Budget** | [**AdBudget**](AdBudget.md) |  | [optional] 
**BudgetLevel** | **string** |  | [optional] 
**Status** | **string** | As in PUT /v1/ads/ad-sets/{adSetId}/status: delivery derived from the switches read back. | [optional] 
**PlatformAdSetStatus** | **string** | The ad set&#39;s own switch read back from the platform; null when it could not be read. | [optional] 
**PlatformCampaignStatus** | **string** |  | [optional] 
**StatusReadAt** | **DateTime?** |  | [optional] 
**StatusUpdated** | **int** | 1 when the ad set&#39;s switch was written. | [optional] 
**StatusSkipped** | **int** | 1 when a live read showed it already in the requested state. | [optional] 
**StatusSkippedReasons** | **List&lt;string&gt;** |  | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal?** |  | [optional] 
**RoasAverageFloor** | **decimal?** |  | [optional] 
**PlatformSpecificData** | **Object** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

