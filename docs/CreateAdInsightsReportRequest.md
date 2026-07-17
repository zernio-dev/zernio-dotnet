# Zernio.Model.CreateAdInsightsReportRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant). | 
**ObjectId** | **string** | Meta insights node: act_&lt;n&gt;, campaign id, ad set id or ad id. | 
**Level** | **string** |  | [optional] 
**Fields** | **string** | Comma-separated Graph insights fields. | [optional] 
**Breakdowns** | **string** | Comma-separated Graph breakdowns. | [optional] 
**Filtering** | [**List&lt;CreateAdInsightsReportRequestFilteringInner&gt;**](CreateAdInsightsReportRequestFilteringInner.md) | Meta filter objects, applied server-side. | [optional] 
**DatePreset** | **string** | Mutually exclusive with fromDate/toDate. | [optional] 
**FromDate** | **DateOnly** |  | [optional] 
**ToDate** | **DateOnly** |  | [optional] 
**TimeIncrement** | [**CreateAdInsightsReportRequestTimeIncrement**](CreateAdInsightsReportRequestTimeIncrement.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

