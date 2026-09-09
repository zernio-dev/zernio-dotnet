# Zernio.Model.ReplaceAdNegativeKeywordListKeywordsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id. | 
**CustomerId** | **string** | Connected Google Ads customer id, without dashes. Required when the connection has multiple customers. | [optional] 
**Platform** | **string** | Optional courtesy field. The resolved account or campaign determines support; other platforms return 501. | [optional] 
**Keywords** | [**List&lt;KeywordEntry&gt;**](KeywordEntry.md) | Full desired keyword set. Bare strings use broad match. Send [] to clear the list. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

