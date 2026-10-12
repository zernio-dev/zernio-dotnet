# Zernio.Model.GetAdReview200ResponseReviewReviewFeedback
Meta only. The Ad's `ad_review_feedback`, verbatim. Both maps are empty when Meta returned no feedback (approved or in-review ad).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Global** | **Dictionary&lt;string, string&gt;** | Meta &#x60;global&#x60;: policy or reason -&gt; Meta&#39;s explanation. | [optional] 
**PlacementSpecific** | **Dictionary&lt;string, Dictionary&lt;string, string&gt;&gt;** | Meta &#x60;placement_specific&#x60;: placement (facebook, instagram, ...) -&gt; reason -&gt; Meta&#39;s explanation. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

