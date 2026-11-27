# Zernio.Model.EditCampaignNegativeKeywordListsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**Platform** | **string** | Optional courtesy field. The resolved account or campaign determines support; other platforms return 501. | [optional] 
**Add** | **List&lt;string&gt;** | Shared negative keyword list ids to attach. Send at least one entry in add or remove. | [optional] 
**Remove** | **List&lt;string&gt;** | Shared negative keyword list ids to detach. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

