# Zernio.Model.GoogleAdLabelAssignments
At least one id across the four target lists. Up to 1000 ids per list.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** | Zernio SocialAccount id (Google Ads) | 
**AdAccountId** | **string** | Google customer id. Required when the connection has multiple customers. | [optional] 
**CustomerId** | **string** | Alias of adAccountId | [optional] 
**CampaignIds** | **List&lt;string&gt;** | Google campaign ids | [optional] 
**AdSetIds** | **List&lt;string&gt;** | Google ad group ids | [optional] 
**AdIds** | **List&lt;string&gt;** | Google ad group ad ids, {adGroupId}~{adId} | [optional] 
**KeywordIds** | **List&lt;string&gt;** | Google keyword criterion ids, {adGroupId}~{criterionId} | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

