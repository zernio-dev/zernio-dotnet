# Zernio.Model.CreatorCampaignEconomicsCpm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Metric** | **string** | What the rate pays on. &#x60;engagements&#x60; counts the &#x60;engagementTypes&#x60; as each platform reports them, and &#x60;minViewsToEarn&#x60; then applies to engagements. Fixed once the campaign leaves draft. | [optional] [default to MetricEnum.Views]
**EngagementTypes** | **List&lt;CreatorCampaignEconomicsCpm.EngagementTypesEnum&gt;** | With &#x60;metric: engagements&#x60;, the engagements that count. Missing means all four, and sending it on a views campaign answers 400. YouTube reports likes and comments only, Facebook and Threads have no saves, and Pinterest reports saves only. | [optional] 
**OrganicViewsOnly** | **bool** | Count only organic views: views from ads the creator ran do not earn. Every campaign platform must be YouTube or X, which report ad views per post, or the request answers 400. A post earns nothing until its ad views were first read. | [optional] [default to false]
**RatePer1kCents** | **int** |  | 
**MinViewsToEarn** | **int** | The count a post must reach before it earns, in the campaign metric (views or engagements). | 
**MaxPayoutPerClipCents** | **int** |  | [optional] 
**BudgetCents** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

