# Zernio.Model.UpdateValueRuleSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stage** | **bool** | Send true to store this write as a staged change instead of applying it. The response is &#x60;202&#x60; with the change, and POST /v1/ads/changes/{changeId}/confirm applies it later. Cannot be combined with &#x60;validateOnly&#x60;. | [optional] 
**AccountId** | **string** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. | 
**Name** | **string** | Required: the update replaces the whole set. | 
**Rules** | [**List&lt;ValueRule&gt;**](ValueRule.md) | The COMPLETE rule list. Omitting a rule deletes it on Meta. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

