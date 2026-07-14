# Zernio.Model.LinkedInAdsPlatformData
LinkedIn campaign bidding and delivery controls for POST /v1/ads/boost and POST /v1/ads/create. Unknown keys are rejected. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CostType** | **string** | Campaign cost model (billing event). Defaults to &#x60;CPM&#x60;. Required when &#x60;unitCost&#x60; is set so the manual bid applies to an explicit cost model.  | [optional] 
**UnitCost** | **decimal** | Manual bid in WHOLE account-currency units (e.g. 2.5 &#x3D; $2.50). Requires &#x60;costType&#x60;. Omit for LinkedIn&#39;s automated (max delivery) bidding. LinkedIn enforces its own per-audience min/max bid bounds.  | [optional] 
**OptimizationTargetType** | **string** | Campaign &#x60;optimizationTargetType&#x60; (e.g. &#x60;MAX_CLICK&#x60;, &#x60;TARGET_COST_PER_CLICK&#x60;, &#x60;MAX_IMPRESSION&#x60;). Forwarded verbatim — LinkedIn validates compatibility with the objective and &#x60;costType&#x60;. Omit for the objective-derived default.  | [optional] 
**CreativeSelection** | **string** | How LinkedIn rotates creatives within the campaign. Defaults to &#x60;OPTIMIZED&#x60;. | [optional] 
**AudienceExpansionEnabled** | **bool** | Enable LinkedIn audience expansion. Defaults to false. | [optional] 
**OffsiteDeliveryEnabled** | **bool** | Deliver on the LinkedIn Audience Network. Defaults to false. | [optional] 
**ConnectedTelevisionOnly** | **bool** | Restrict delivery to Connected TV inventory. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

