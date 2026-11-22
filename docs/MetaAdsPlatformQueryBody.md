# Zernio.Model.MetaAdsPlatformQueryBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The Zernio id of the connected Meta ads account. | 
**AdAccountId** | **string** | The Meta ad account, act_&lt;n&gt;. Read its campaigns, ad sets or ads with level and filtering. | 
**Level** | **string** | The level of each row. Defaults to the ad account. | [optional] 
**Fields** | **List&lt;string&gt;** | Meta insights fields, such as spend or impressions, up to 100. | [optional] 
**Breakdowns** | **List&lt;string&gt;** | Meta breakdowns, up to 5. | [optional] 
**ActionBreakdowns** | **List&lt;string&gt;** | An empty array asks Meta for no action breakdown at all. | [optional] 
**ActionAttributionWindows** | **List&lt;string&gt;** | Meta attribution windows, such as 7d_click or 1d_view. | [optional] 
**ActionReportTime** | **string** | impression, conversion or mixed. | [optional] 
**UseUnifiedAttributionSetting** | **bool** | Use each ad set&#39;s own attribution setting. | [optional] 
**Filtering** | [**List&lt;MetaAdsPlatformQueryBodyFilteringInner&gt;**](MetaAdsPlatformQueryBodyFilteringInner.md) | Meta filters of field, operator and value, up to 25. | [optional] 
**DatePreset** | **string** | A Meta date preset, such as last_30d. Not with fromDate and toDate. | [optional] 
**FromDate** | **DateOnly** | First day, YYYY-MM-DD, sent with toDate. | [optional] 
**ToDate** | **DateOnly** | Last day, YYYY-MM-DD, sent with fromDate. | [optional] 
**TimeIncrement** | [**MetaAdsPlatformQueryBodyTimeIncrement**](MetaAdsPlatformQueryBodyTimeIncrement.md) |  | [optional] 
**Limit** | **int** | Rows per page, up to 500. Defaults to 500. | [optional] [default to 500]
**Cursor** | **string** | The pagination.nextCursor of the previous page, unchanged. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

