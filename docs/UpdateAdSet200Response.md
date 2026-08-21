# Zernio.Model.UpdateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Budget** | [**AdBudget**](AdBudget.md) |  | [optional] 
**BudgetLevel** | **string** |  | [optional] 
**Status** | **string** | The status written to the ad set. Absent when nothing was written (see statusMessage). | [optional] 
**StatusUpdated** | **int** | Number of ads whose own stored status changed alongside the ad set switch | [optional] 
**StatusSkipped** | **int** | Number of ads whose own status was left as it was | [optional] 
**StatusSkippedReasons** | **List&lt;string&gt;** | Why each group of ads was skipped | [optional] 
**StatusMessage** | **string** | Present only where the platform has no ad-set switch and no child ad was actionable; &#x60;status&#x60; is then absent because nothing was written | [optional] 
**BidStrategy** | **BidStrategy** |  | [optional] 
**BidAmount** | **decimal?** |  | [optional] 
**RoasAverageFloor** | **decimal?** |  | [optional] 
**PlatformSpecificData** | **Object** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

