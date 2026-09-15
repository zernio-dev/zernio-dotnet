# Zernio.Model.AdKeywordQuality
Google Quality Score and the three component ratings behind it (`ad_group_criterion.quality_info`). Every field is null until Google has rated the keyword: a keyword with too little traffic is unrated, and negatives are never rated. Google's own UNKNOWN / UNSPECIFIED buckets are reported as null so \"unrated\" has a single representation. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Score** | **int?** | Quality Score, 1-10. | [optional] 
**ExpectedCtr** | **string** | How the click-through rate compares with other ads in the same position (&#x60;search_predicted_ctr&#x60;). | [optional] 
**AdRelevance** | **string** | How closely the ad matches the intent behind the search (&#x60;creative_quality_score&#x60;). | [optional] 
**LandingPageExperience** | **string** | How relevant and useful the landing page is to people who click (&#x60;post_click_quality_score&#x60;). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

