# Zernio.Model.UpdateAdSetRequestPlatformSpecificData
Platform-specific post-launch delivery settings. The platform is implied by the `platform` body param. Meta only; other platforms return 400. Unknown keys are rejected. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OptimizationGoal** | **string** | Meta ad-set optimization_goal (e.g. OFFSITE_CONVERSIONS, LANDING_PAGE_VIEWS). | [optional] 
**BillingEvent** | **string** | Meta ad-set billing_event (e.g. IMPRESSIONS, LINK_CLICKS, THRUPLAY). | [optional] 
**StartDate** | **string** | Ad set start_time (ISO 8601). | [optional] 
**EndDate** | **string** | Ad set end_time (ISO 8601). | [optional] 
**PromotedObject** | [**UpdateAdSetRequestPlatformSpecificDataPromotedObject**](UpdateAdSetRequestPlatformSpecificDataPromotedObject.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

