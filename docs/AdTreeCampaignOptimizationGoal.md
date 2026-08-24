# Zernio.Model.AdTreeCampaignOptimizationGoal
A single string when every ad set shares one optimization goal; a JSON array of the distinct goals when ad sets differ (never a comma-joined string); array element order is not guaranteed, treat it as an unordered set; the key is absent when no ad set carries a goal. Meta: e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION. LinkedIn: the campaign optimizationTargetType (e.g. MAX_CLICK, MAX_IMPRESSION, NONE); `NONE` with a manual costType is a campaign LinkedIn will not deliver.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

