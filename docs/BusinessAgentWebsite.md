# Zernio.Model.BusinessAgentWebsite

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Url** | **string** |  | 
**IncludedSubDomains** | **List&lt;string&gt;** |  | [optional] 
**IncludedUrlPatterns** | **List&lt;string&gt;** | Only URLs containing one of these substrings are ingested. | [optional] 
**ExcludedSubDomains** | **List&lt;string&gt;** |  | [optional] 
**ExcludedUrlPatterns** | **List&lt;string&gt;** |  | [optional] 
**SingleUrls** | **List&lt;string&gt;** | Crawl only these exact pages instead of the whole site. | [optional] 
**Id** | **string** |  | 
**CrawlStatus** | **string** | not_started, pending, in_progress, completed, completed_no_data or failed (see crawl_error). | [optional] 
**CrawlError** | **string** |  | [optional] 
**PagesCrawled** | **int** |  | [optional] 
**LastCrawledAt** | **int** | Unix seconds. | [optional] 
**CreatedAt** | **int** | Unix seconds. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

