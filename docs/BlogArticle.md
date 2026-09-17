# Zernio.Model.BlogArticle
An article inside a blog on the connected platform.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native numeric article/post id. | [optional] 
**BlogId** | **string** | Platform-native id of the blog the article belongs to. | [optional] 
**Platform** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**BodyHtml** | **string** | Article body as HTML. | [optional] 
**Handle** | **string** | URL slug of the article. | [optional] 
**Tags** | **List&lt;string&gt;** | Tag names. On WordPress, missing tag names are created and matching is case-insensitive. | [optional] 
**Author** | **string** | Shopify author display name, or numeric WordPress user id serialized as a string. | [optional] 
**Excerpt** | **string** | Short summary shown in blog listings. | [optional] 
**Image** | [**BlogArticleImage**](BlogArticleImage.md) |  | [optional] 
**IsPublished** | **bool** | False while the article is a draft or its publish date is still in the future. | [optional] 
**PublishedAt** | **DateTime?** | Publication time. On WordPress this is present only when status is &#x60;publish&#x60;; null for drafts, pending/private posts, and scheduled posts. | [optional] 
**Status** | **string** | WordPress only. Native post status returned by WordPress; omitted for Shopify. | [optional] 
**PublishDate** | **DateTime?** | WordPress only. Scheduled publication time in UTC when status is &#x60;future&#x60;; null for other WordPress statuses and omitted for Shopify. | [optional] 
**CreatedAt** | **DateTime?** | Creation time when the platform exposes one. WordPress returns null because its core date is the editable publication date. | [optional] 
**UpdatedAt** | **DateTime?** | Last modification time. WordPress returns modified_gmt as UTC. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

