# Zernio.Model.EditAdNegativeKeywordListKeywordsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id. | 
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. | [optional] 
**CustomerId** | **string** | Alias of adAccountId, kept for existing callers | [optional] 
**Platform** | **string** | Optional courtesy field. The resolved account or campaign determines support; other platforms return 501. | [optional] 
**Add** | [**List&lt;KeywordEntry&gt;**](KeywordEntry.md) | Keywords to add. Send at least one entry in add or remove. | [optional] 
**Remove** | [**List&lt;KeywordEntry&gt;**](KeywordEntry.md) | Keywords to remove. Bare strings mean broad match. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

