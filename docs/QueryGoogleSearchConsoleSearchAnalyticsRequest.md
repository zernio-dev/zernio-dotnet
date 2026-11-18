# Zernio.Model.QueryGoogleSearchConsoleSearchAnalyticsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio account ID of the Google Search Console connection. | 
**FromDate** | **DateOnly** |  | [optional] 
**ToDate** | **DateOnly** |  | [optional] 
**Dimensions** | **List&lt;QueryGoogleSearchConsoleSearchAnalyticsRequest.DimensionsEnum&gt;** |  | [optional] 
**Type** | **string** | Which Google surface to read. Defaults to &#x60;web&#x60;. | [optional] 
**DimensionFilterGroups** | [**List&lt;QueryGoogleSearchConsoleSearchAnalyticsRequestDimensionFilterGroupsInner&gt;**](QueryGoogleSearchConsoleSearchAnalyticsRequestDimensionFilterGroupsInner.md) |  | [optional] 
**AggregationType** | **string** |  | [optional] 
**RowLimit** | **int** | Defaults to 1000. | [optional] 
**StartRow** | **int** | Row offset for paging past &#x60;rowLimit&#x60;. | [optional] 
**DataState** | **string** | &#x60;final&#x60; (default) leaves out the last two or three days; &#x60;all&#x60; includes them while Google is still filling them in; &#x60;hourly_all&#x60; is required with the &#x60;hour&#x60; dimension. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

