# Zernio.Model.CreateBlogArticleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** |  | 
**BodyHtml** | **string** | Article body as HTML. | [optional] 
**Handle** | **string** | URL slug. Generated from the title when omitted. | [optional] 
**Tags** | **List&lt;string&gt;** | Tag names. WordPress and Wix resolve existing names case-insensitively and create missing tags (Wix allows up to 30). | [optional] 
**Author** | **string** | Shopify author display name, numeric WordPress user id serialized as a string, or Wix site member id. Assigning another WordPress user may require elevated capability. Wix posts without one go to the site&#39;s default author. | [optional] 
**Excerpt** | **string** | Short summary shown in blog listings. | [optional] 
**Image** | [**CreateBlogArticleRequestImage**](CreateBlogArticleRequestImage.md) |  | [optional] 
**Seo** | [**CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md) |  | [optional] 
**IsPublished** | **bool** | Set false for a draft or true to publish. On WordPress and Wix false takes priority over a future publishDate; omission with no date defaults to draft. | [optional] 
**PublishDate** | **DateTime** | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

