# Zernio.Model.ListSmsSenderIds200ResponseBudget
Workspace-wide daily sending budget, shared by every sender ID (resets midnight UTC).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Cap** | **int** | Daily message cap (raisable via &#x60;/v1/sms/sender-ids/limit-request&#x60;). | [optional] 
**UsedToday** | **int** | Messages already counted against today&#39;s cap. | [optional] 
**Level** | **int** | Cap tier (Level 1 &#x3D; 500/day). | [optional] 
**PendingRequest** | [**ListSmsSenderIds200ResponseBudgetPendingRequest**](ListSmsSenderIds200ResponseBudgetPendingRequest.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

