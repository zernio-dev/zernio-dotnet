# Zernio.Model.UpdateBlogArticleRequest
At least one field is required.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | [optional] 
**BodyHtml** | **string** | Article body as HTML. | [optional] 
**Handle** | **string** | URL slug of the article. | [optional] 
**Tags** | **List&lt;string&gt;** | Replaces the full tag list. | [optional] 
**Author** | **string** | Display name of the article author. | [optional] 
**Excerpt** | **string** | Short summary shown in blog listings. | [optional] 
**Image** | [**CreateBlogArticleRequestImage**](CreateBlogArticleRequestImage.md) |  | [optional] 
**Seo** | [**CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md) |  | [optional] 
**IsPublished** | **bool** | Set false to unpublish the article back to a draft. | [optional] 
**PublishDate** | **DateTime** | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

