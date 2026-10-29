# Zernio.Model.CreateStandaloneAd201ResponseOneOf1
Multi-creative shape: N ads returned sharing platformCampaignId / platformAdSetId.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ads** | [**List&lt;Ad&gt;**](Ad.md) |  | [optional] 
**PlatformCampaignId** | **string** |  | [optional] 
**PlatformAdSetId** | **string** |  | [optional] 
**AppliedDefaults** | [**AdAppliedDefaults**](AdAppliedDefaults.md) |  | [optional] 
**Message** | **string** |  | [optional] 
**Warnings** | **List&lt;string&gt;** | Meta only, present only when needed.  An &#x60;activation_failed:&#x60; entry means Meta refused the final switch to ACTIVE for the ads it names (or for their ad set or campaign). The entry names what was kept PAUSED and what was switched ACTIVE, and quotes Meta&#39;s error and the status calls that switch the PAUSED ones on later.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

