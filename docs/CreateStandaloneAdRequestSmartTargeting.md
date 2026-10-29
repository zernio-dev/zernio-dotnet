# Zernio.Model.CreateStandaloneAdRequestSmartTargeting
TikTok only (a 400 elsewhere). TikTok Smart Targeting on the ad group. When on, TikTok may deliver beyond the selected audiences or interests.  - `audience`: TikTok's `smart_audience_enabled`. - `interestsBehaviors`: TikTok's `smart_interest_behavior_enabled`.  Available on Video views, Traffic, Lead generation, App install, Web conversion and Community interaction. Not available with smartPlus or when attaching to an existing ad set (adSetId).  Only the flags you send are written. An unwritten flag reads back null in `nativeSettings`, so send `false` explicitly to be able to verify it is off. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Audience** | **bool** | TikTok smart_audience_enabled. | [optional] 
**InterestsBehaviors** | **bool** | TikTok smart_interest_behavior_enabled. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

