# Zernio.Model.UpdateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Budget** | [**AdBudget**](AdBudget.md) |  | [optional] 
**BudgetLevel** | **string** |  | [optional] 
**Status** | **string** | The status written to the ad set switch | [optional] 
**StatusUpdated** | **int** | Number of ads whose own stored status changed alongside the ad set switch | [optional] 
**StatusSkipped** | **int** | Number of ads whose own status was left as it was | [optional] 
**StatusSkippedReasons** | **List&lt;string&gt;** | Why each group of ads was skipped | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal?** |  | [optional] 
**RoasAverageFloor** | **decimal?** |  | [optional] 
**PlatformSpecificData** | **Object** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

