# Zernio.Model.UpdateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Budget** | [**AdBudget**](AdBudget.md) |  | [optional] 
**BudgetLevel** | **string** |  | [optional] 
**Status** | **string** | As in PUT /v1/ads/ad-sets/{adSetId}/status: delivery derived from the switches read back. | [optional] 
**PlatformAdSetStatus** | **string** | The ad set&#39;s status read back from the platform, as in PUT /v1/ads/ad-sets/{adSetId}/status (Meta and Reddit return the ad set&#39;s effective_status); null when it could not be read. | [optional] 
**PlatformCampaignStatus** | **string** |  | [optional] 
**StatusReadAt** | **DateTime?** |  | [optional] 
**StatusUpdated** | **int** | 1 when the ad set&#39;s switch was written. | [optional] 
**StatusSkipped** | **int** | 1 when a live read showed it already in the requested state. | [optional] 
**StatusSkippedReasons** | **List&lt;string&gt;** |  | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal?** |  | [optional] 
**RoasAverageFloor** | **decimal?** |  | [optional] 
**PlatformSpecificData** | **Object** |  | [optional] 
**Targeting** | **Object** | Present when &#x60;placements&#x60; or &#x60;targeting&#x60; was sent. The ad set&#39;s full targeting as written, in the platform&#39;s own vocabulary (Meta or Reddit snake_case). Stored as the ad set&#39;s &#x60;targeting&#x60;. Meta stores the same object on its ads; Reddit stores it on its ads in the create vocabulary (&#x60;countries&#x60;, &#x60;communities&#x60;, ...), as GET /v1/ads/ad-sets/{adSetId}/targeting returns it. | [optional] 
**StartDate** | **string** | Reddit: the start_time written, a UTC instant. Present when &#x60;startDate&#x60; was sent. | [optional] 
**EndDate** | **string** | Reddit: the end_time written, a UTC instant, or null when the end date was removed. Present when &#x60;endDate&#x60; was sent. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

