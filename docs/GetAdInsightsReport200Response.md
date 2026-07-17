# Zernio.Model.GetAdInsightsReport200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ReportRunId** | **string** |  | [optional] 
**Status** | **string** | Meta async_status: Job Not Started, Job Started, Job Running, Job Completed, Job Failed, Job Skipped. | [optional] 
**PercentCompletion** | **int** |  | [optional] 
**DateStart** | **string** |  | [optional] 
**DateStop** | **string** |  | [optional] 
**Data** | **List&lt;Object&gt;** | Present only when status is Job Completed. | [optional] 
**Paging** | [**GetAdInsightsReport200ResponsePaging**](GetAdInsightsReport200ResponsePaging.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

