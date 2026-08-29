# Zernio.Model.AttachCampaignAssetsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio Google Ads SocialAccount id — resolves the customer id + refresh token. | 
**CustomerId** | **string** | Numeric Google Ads customer id. Required when the connection has multiple Google Ads accounts; optional (and inferred) when it has only one. | [optional] 
**Sitelinks** | [**List&lt;AttachCampaignAssetsRequestSitelinksInner&gt;**](AttachCampaignAssetsRequestSitelinksInner.md) | See POST /v1/ads/create sitelinks — same shape. | [optional] 
**Callouts** | **List&lt;string&gt;** |  | [optional] 
**StructuredSnippets** | [**List&lt;AttachCampaignAssetsRequestStructuredSnippetsInner&gt;**](AttachCampaignAssetsRequestStructuredSnippetsInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

