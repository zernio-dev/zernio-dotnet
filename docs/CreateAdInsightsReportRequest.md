# Zernio.Model.CreateAdInsightsReportRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant). | 
**ObjectId** | **string** | Meta insights node: act_&lt;n&gt;, campaign id, ad set id or ad id. | 
**Level** | **string** |  | [optional] 
**Fields** | **string** | Comma-separated Graph insights fields. | [optional] 
**Breakdowns** | **string** | Comma-separated Graph breakdowns. | [optional] 
**ActionBreakdowns** | **string** | Comma-separated Graph action breakdowns (e.g. action_type,action_destination). | [optional] 
**ActionAttributionWindows** | **List&lt;string&gt;** | Meta attribution windows (e.g. [\&quot;7d_click\&quot;, \&quot;1d_view\&quot;]). Action values are returned keyed per window. | [optional] 
**ActionReportTime** | **string** | When actions are counted: impression, conversion or mixed. | [optional] 
**UseUnifiedAttributionSetting** | **bool** | Use the ad sets&#39; own attribution settings for action counting. | [optional] 
**Filtering** | [**List&lt;CreateAdInsightsReportRequestFilteringInner&gt;**](CreateAdInsightsReportRequestFilteringInner.md) | Meta filter objects, applied server-side. | [optional] 
**DatePreset** | **string** | Mutually exclusive with fromDate/toDate. | [optional] 
**FromDate** | **DateOnly** |  | [optional] 
**ToDate** | **DateOnly** |  | [optional] 
**TimeIncrement** | [**CreateAdInsightsReportRequestTimeIncrement**](CreateAdInsightsReportRequestTimeIncrement.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

