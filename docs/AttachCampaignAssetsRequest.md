# Zernio.Model.AttachCampaignAssetsRequest
Provide at least one of sitelinks, callouts, structuredSnippets or images. Sitelink description1 and description2 must be supplied together.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio Google Ads connection id. | 
**AdAccountId** | **string** | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. | [optional] 
**CustomerId** | **string** | Alias of adAccountId, kept for existing callers | [optional] 
**Sitelinks** | [**List&lt;GoogleSitelink&gt;**](GoogleSitelink.md) |  | [optional] 
**Callouts** | **List&lt;string&gt;** |  | [optional] 
**StructuredSnippets** | [**List&lt;GoogleStructuredSnippet&gt;**](GoogleStructuredSnippet.md) |  | [optional] 
**Images** | **List&lt;string&gt;** | Public image URLs, uploaded to Google as image assets. Landscape 1.91:1 (min 600x314) or square 1:1 (min 300x300), up to 5 MB each. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

