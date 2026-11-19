# Zernio.Model.GetEvent200ResponseTouchesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**At** | **DateTime** |  | [optional] 
**Kind** | **string** |  | [optional] 
**Platform** | **string** | The ad platform of the campaign, or the one a survey answer names (Instagram reads as facebook). | [optional] 
**AdAccountId** | **string** |  | [optional] 
**CampaignId** | **string** | The campaign the touch resolved to; null for a touch that named none (search, referral). | [optional] 
**Credit** | **Dictionary&lt;string, decimal&gt;** | The share of the event (0 to 1) this touch gets per model: first_touch, last_non_direct, linear, position_based, time_decay, w_shaped. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

