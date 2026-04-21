# Late.Model.GetAdAnalytics200ResponseAnalyticsDailyInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Spend** | **decimal** |  | [optional] 
**Impressions** | **int** |  | [optional] 
**Reach** | **int** |  | [optional] 
**Clicks** | **int** |  | [optional] 
**Ctr** | **decimal** | Click-through rate (%) | [optional] 
**Cpc** | **decimal** | Cost per click | [optional] 
**Cpm** | **decimal** | Cost per 1000 impressions | [optional] 
**Engagement** | **int** |  | [optional] 
**Conversions** | **int** | Count of conversion events matching the campaign&#39;s promoted_object.custom_event_type (PURCHASE, LEAD, etc.) over the requested date range. 0 for non-conversion campaigns or when no events have fired. Meta-only at time of writing; other platforms return 0. | [optional] 
**CostPerConversion** | **decimal** | Derived spend / conversions in the same currency as spend. 0 when conversions is 0. | [optional] 
**Actions** | **Dictionary&lt;string, int&gt;** | Raw per-action-type counts from Meta&#39;s Insights actions[] array, summed over the date range. Keys are Meta action_type strings (e.g. link_click, offsite_conversion.fb_pixel_purchase, onsite_conversion.lead_grouped). Use this to extract any conversion event (purchases, leads, add_to_cart, etc.) without relying on the derived conversions field. Empty object when no actions are reported. | [optional] 
**LastSyncedAt** | **DateTime** | Present on individual ads only, not on campaign aggregations | [optional] 
**Date** | **DateOnly** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

