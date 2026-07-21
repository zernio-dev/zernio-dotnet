# Zernio.Model.CreateRfPredictionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant). | 
**AdAccountId** | **string** | Meta ad account id (act_&lt;n&gt;). | 
**BudgetAmount** | **decimal** | Whole currency units. Exactly one of budgetAmount / reach. | [optional] 
**Reach** | **int** | Target unique reach. Exactly one of budgetAmount / reach. | [optional] 
**StartDate** | **DateTime** | Campaign window start (must be in the future). | 
**EndDate** | **DateTime** |  | 
**FrequencyCap** | **int** | Max impressions per person over the window. | [optional] 
**Targeting** | **Object** | Canonical camelCase TargetingSpec (same shape as /v1/ads/create&#39;s &#x60;targeting&#x60;). Defaults to countries: [US]. | [optional] 
**Placements** | **Object** | Meta placements object (same shape as /v1/ads/create&#39;s &#x60;placements&#x60;). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

