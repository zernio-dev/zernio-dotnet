# Zernio.Model.TikTokAdsPlatformQueryBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The Zernio id of the connected TikTok ads account. | 
**AdAccountId** | **string** | The numeric TikTok advertiser id. | 
**ReportType** | **string** | Defaults to BASIC. | [optional] [default to ReportTypeEnum.BASIC]
**DataLevel** | **string** | The level of each row. | 
**Dimensions** | **List&lt;string&gt;** | TikTok dimensions, 1 to 4. | 
**Metrics** | **List&lt;string&gt;** | TikTok metrics, up to 100. | 
**Filtering** | [**List&lt;MetaAdsPlatformQueryBodyFilteringInner&gt;**](MetaAdsPlatformQueryBodyFilteringInner.md) | TikTok filters of field, operator and value, up to 25. A filter on an entity finer than dataLevel is refused. | [optional] 
**FromDate** | **DateOnly** | First day, YYYY-MM-DD, inclusive. | 
**ToDate** | **DateOnly** | Last day, YYYY-MM-DD, inclusive. | 
**PageSize** | **int** | Rows per page, up to 1,000. Defaults to 1,000. | [optional] [default to 1000]
**Cursor** | **string** | The pagination.nextCursor of the previous page, unchanged. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

