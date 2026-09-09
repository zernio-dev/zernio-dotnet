# Zernio.Model.AttachCampaignAssetsRequest
Provide at least one of sitelinks, callouts or structuredSnippets. Sitelink description1 and description2 must be supplied together.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio Google Ads connection id. | 
**CustomerId** | **string** | Google customer id without dashes. Required when the connection has multiple customers. | [optional] 
**Sitelinks** | [**List&lt;GoogleSitelink&gt;**](GoogleSitelink.md) |  | [optional] 
**Callouts** | **List&lt;string&gt;** |  | [optional] 
**StructuredSnippets** | [**List&lt;GoogleStructuredSnippet&gt;**](GoogleStructuredSnippet.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

