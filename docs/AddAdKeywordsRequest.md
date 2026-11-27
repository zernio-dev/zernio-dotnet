# Zernio.Model.AddAdKeywordsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** | Account ID (Google Ads) | 
**AdSetId** | **string** | Google ad group ID to add the keywords to | 
**Keywords** | [**List&lt;AddAdKeywordsRequestKeywordsInner&gt;**](AddAdKeywordsRequestKeywordsInner.md) |  | 
**Negative** | **bool** | Add as ad-group-level negatives instead of positive keywords | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

