# Zernio.Model.UpdateCampaignTargeting200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CampaignId** | **string** |  | [optional] 
**AdGroupId** | **string** | Demand Gen only: the ad group that received the locations and languages. | [optional] 
**Updated** | **List&lt;UpdateCampaignTargeting200Response.UpdatedEnum&gt;** | Which targeting fields were applied. | [optional] 
**LocationTargetingType** | **string** | The value read back from Google after the edit. | [optional] 
**Devices** | [**List&lt;UpdateCampaignTargeting200ResponseDevicesInner&gt;**](UpdateCampaignTargeting200ResponseDevicesInner.md) |  | [optional] 
**Locations** | [**List&lt;UpdateCampaignTargeting200ResponseLocationsInner&gt;**](UpdateCampaignTargeting200ResponseLocationsInner.md) |  | [optional] 
**ExcludedLocations** | [**List&lt;UpdateCampaignTargeting200ResponseExcludedLocationsInner&gt;**](UpdateCampaignTargeting200ResponseExcludedLocationsInner.md) | The negative (excluded) location criteria read back after the edit, same item shape as &#x60;locations&#x60;. | [optional] 
**Languages** | [**List&lt;UpdateCampaignTargeting200ResponseLanguagesInner&gt;**](UpdateCampaignTargeting200ResponseLanguagesInner.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

