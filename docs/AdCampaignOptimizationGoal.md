# Zernio.Model.AdCampaignOptimizationGoal
The campaign's optimization goal.  - Every ad set shares one goal: a single string. - Ad sets differ: a JSON array of the distinct goals (never a comma-joined string). Element order is not guaranteed; treat it as an unordered set. - No ad set carries a goal: the key is absent.  **Values:**  - Meta: e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION. - LinkedIn: the campaign optimizationTargetType (e.g. MAX_CLICK, MAX_IMPRESSION, NONE). `NONE` with a manual costType is a campaign LinkedIn will not deliver. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

