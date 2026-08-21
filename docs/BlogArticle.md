# Zernio.Model.BlogArticle
An article inside a blog on the connected platform.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native article id (numeric string for Shopify). | [optional] 
**BlogId** | **string** | Platform-native id of the blog the article belongs to. | [optional] 
**Platform** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**BodyHtml** | **string** | Article body as HTML. | [optional] 
**Handle** | **string** | URL slug of the article. | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**Author** | **string** | Display name of the article author. | [optional] 
**Excerpt** | **string** | Short summary shown in blog listings. | [optional] 
**Image** | [**BlogArticleImage**](BlogArticleImage.md) |  | [optional] 
**IsPublished** | **bool** | False while the article is a draft or its publish date is still in the future. | [optional] 
**PublishedAt** | **DateTime?** | When the article was (or is scheduled to be) published; null for drafts. | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 
**UpdatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

