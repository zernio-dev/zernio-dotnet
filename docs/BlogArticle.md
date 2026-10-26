# Zernio.Model.BlogArticle
An article inside a blog on the connected platform.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform-native article/post id: numeric on Shopify and WordPress, a GUID on Wix, a hex item id on Webflow. | [optional] 
**BlogId** | **string** | Platform-native id of the blog the article belongs to. | [optional] 
**Platform** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**BodyHtml** | **string** | Article body as HTML. Wix stores rich content, converted from and to HTML; Wix lists return null (get the article for its body). | [optional] 
**Handle** | **string** | URL slug of the article. | [optional] 
**Url** | **string** | WordPress and Wix. Public URL of the article while it is published; null for drafts and scheduled posts, and on a Wix site that is not published yet. | [optional] 
**Tags** | **List&lt;string&gt;** | Tag names. On WordPress and Wix, missing tag names are created and matching is case-insensitive. | [optional] 
**Author** | **string** | Shopify author display name, numeric WordPress user id serialized as a string, or Wix site member id. Wix posts without one are attributed to the site&#39;s default author. | [optional] 
**Excerpt** | **string** | Short summary shown in blog listings. | [optional] 
**Image** | [**BlogArticleImage**](BlogArticleImage.md) |  | [optional] 
**IsPublished** | **bool** | False while the article is a draft or its publish date is still in the future. | [optional] 
**PublishedAt** | **DateTime?** | Publication time. On WordPress this is present only when status is &#x60;publish&#x60;; null for drafts, pending/private posts, and scheduled posts. | [optional] 
**Status** | **string** | WordPress and Wix. Post status (&#x60;future&#x60; &#x3D; scheduled, &#x60;pending&#x60; &#x3D; in review on Wix); omitted for Shopify. | [optional] 
**PublishDate** | **DateTime?** | WordPress and Wix. Scheduled publication time in UTC when status is &#x60;future&#x60;; null for other statuses and omitted for Shopify. | [optional] 
**CreatedAt** | **DateTime?** | Creation time when the platform exposes one. WordPress returns null because its core date is the editable publication date. | [optional] 
**UpdatedAt** | **DateTime?** | Last modification time. WordPress returns modified_gmt as UTC. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

