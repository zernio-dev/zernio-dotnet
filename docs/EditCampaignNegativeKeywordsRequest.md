# Zernio.Model.EditCampaignNegativeKeywordsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** | Optional and NOT authoritative: the resolved campaign&#39;s own platform decides 200 vs 501, never this hint. | [optional] 
**Add** | [**List&lt;KeywordEntry&gt;**](KeywordEntry.md) | Negative keywords to add. Send at least one entry in add or remove. | [optional] 
**Remove** | [**List&lt;KeywordEntry&gt;**](KeywordEntry.md) | Negative keywords to remove. Bare strings mean broad match. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

