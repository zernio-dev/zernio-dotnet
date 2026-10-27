# Zernio.Model.CreateStandaloneAd201ResponseOneOf
Legacy + attach shapes: one ad returned.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ad** | [**Ad**](Ad.md) |  | [optional] 
**AppliedDefaults** | [**AdAppliedDefaults**](AdAppliedDefaults.md) |  | [optional] 
**Message** | **string** |  | [optional] 
**Warnings** | **List&lt;string&gt;** | Meta only, present only when needed. An &#x60;activation_failed:&#x60; entry means Meta refused the final switch to ACTIVE: the entry names what was kept PAUSED (the ad, and its ad set or campaign when Meta refused those) and what was switched ACTIVE, and quotes Meta&#39;s error and the status calls that switch the PAUSED ones on later. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

