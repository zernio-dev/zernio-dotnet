# Zernio.Model.GenerateKeywordIdeasRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio googleads SocialAccount id. | 
**CustomerId** | **string** | Numeric Google Ads customer id (no dashes); only needed when the connection has several accounts. | [optional] 
**SeedKeywords** | **List&lt;string&gt;** | Seed terms. Provide these, seedUrl, or both. | [optional] 
**SeedUrl** | **string** | Landing page to mine for ideas. Provide this, seedKeywords, or both. | [optional] 
**Countries** | **List&lt;string&gt;** | ISO 3166-1 alpha-2 country codes. Omitted &#x3D; worldwide. | [optional] 
**LanguageConstantId** | **string** | Google languageConstant id (1000 &#x3D; English). | [optional] [default to "1000"]
**Network** | **string** |  | [optional] [default to NetworkEnum.GOOGLESEARCH]
**IncludeAdultKeywords** | **bool** |  | [optional] 
**PageSize** | **int** |  | [optional] 
**PageToken** | **string** | Cursor from paging.nextPageToken of the previous page. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

