# Zernio.Model.CampaignAnalyticsResponseCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Status** | **string** | The platform&#39;s own campaign status in its vocabulary (Google ENABLED / PAUSED / REMOVED, Meta ACTIVE / PAUSED, ...), the same value as platformCampaignStatus on /v1/ads/campaigns and /v1/ads/tree. For a campaign synced before that value was stored it falls back to an active child ad&#39;s status, else the newest ad&#39;s. | [optional] 
**Budget** | [**AdCampaignBudget**](AdCampaignBudget.md) |  | [optional] 
**Currency** | **string** | ISO 4217 code of the ad account (e.g. USD, THB). All money values in &#x60;summary&#x60; and &#x60;daily&#x60; are in this currency. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

