# Zernio.Model.UpdateBlogArticleRequest
At least one field is required.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | [optional] 
**BodyHtml** | **string** | Article body as HTML. | [optional] 
**Handle** | **string** | URL slug of the article. | [optional] 
**Tags** | **List&lt;string&gt;** | Replaces the full tag-name list. WordPress resolves existing names case-insensitively and creates missing tags. | [optional] 
**Author** | **string** | Shopify author display name, or numeric WordPress user id serialized as a string. Assigning another WordPress user may require elevated capability. | [optional] 
**Excerpt** | **string** | Short summary shown in blog listings. | [optional] 
**Image** | [**UpdateBlogArticleRequestImage**](UpdateBlogArticleRequestImage.md) |  | [optional] 
**Seo** | [**CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md) |  | [optional] 
**IsPublished** | **bool** | Set false to move to draft or true to publish. On WordPress false takes priority over a future publishDate; omission preserves status unless publishDate is sent. | [optional] 
**PublishDate** | **DateTime** | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

