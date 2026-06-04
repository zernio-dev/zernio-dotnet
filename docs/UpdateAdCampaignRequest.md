# Zernio.Model.UpdateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** |  | 
**Budget** | [**UpdateAdCampaignRequestBudget**](UpdateAdCampaignRequestBudget.md) |  | [optional] 
**BidStrategy** | **BidStrategy** | Campaign-level default. Ad sets inherit this unless they override. | [optional] 
**Name** | **string** | Rename the campaign (Meta only; other platforms return 501). At least one of budget/bidStrategy/name is required. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

