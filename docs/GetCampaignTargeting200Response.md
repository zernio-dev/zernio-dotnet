# Zernio.Model.GetCampaignTargeting200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Devices** | [**List&lt;GetCampaignTargeting200ResponseDevicesInner&gt;**](GetCampaignTargeting200ResponseDevicesInner.md) |  | [optional] 
**Locations** | [**List&lt;GetCampaignTargeting200ResponseLocationsInner&gt;**](GetCampaignTargeting200ResponseLocationsInner.md) |  | [optional] 
**Languages** | [**List&lt;GetCampaignTargeting200ResponseLanguagesInner&gt;**](GetCampaignTargeting200ResponseLanguagesInner.md) |  | [optional] 
**CachedAt** | **DateTime?** | When this targeting was fetched from Google. Null when it was never served from cache. | [optional] 
**Stale** | **bool** | True when Google&#39;s daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

