# Zernio.Model.UpdateAdSetRequestSmartTargeting
TikTok only (a 400 elsewhere). TikTok Smart Targeting on the ad group: `audience` is TikTok's `smart_audience_enabled`, `interestsBehaviors` its `smart_interest_behavior_enabled`. When on, TikTok may deliver beyond the selected audiences or interests. Available on Video views, Traffic, Lead generation, App install, Web conversion and Community interaction. Only the flags you send are written; an unwritten flag reads back null in `nativeSettings`, so send `false` explicitly to be able to verify it is off. Applied with TikTok's adgroup/update; read it back with GET /v1/ads/ad-sets?adSetId=...&live=true. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Audience** | **bool** | TikTok smart_audience_enabled. | [optional] 
**InterestsBehaviors** | **bool** | TikTok smart_interest_behavior_enabled. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

