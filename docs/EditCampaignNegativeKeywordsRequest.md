# Zernio.Model.EditCampaignNegativeKeywordsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Platform** | **string** | Optional and NOT authoritative: the resolved campaign&#39;s own platform decides 200 vs 501, never this hint. | [optional] 
**Add** | [**List&lt;KeywordEntry&gt;**](KeywordEntry.md) | Negative keywords to add. Send at least one entry in add or remove. | [optional] 
**Remove** | [**List&lt;KeywordEntry&gt;**](KeywordEntry.md) | Negative keywords to remove. Bare strings mean broad match. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

