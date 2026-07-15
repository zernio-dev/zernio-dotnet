# Zernio.Model.GetAdsTimeline200ResponseRowsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **DateOnly** |  | [optional] 
**Spend** | **decimal** | Native currency units (matches /ads/tree convention). | [optional] 
**Impressions** | **int** |  | [optional] 
**Reach** | **int** |  | [optional] 
**Clicks** | **int** |  | [optional] 
**Engagement** | **int** |  | [optional] 
**Ctr** | **decimal** | Click-through rate as a percentage (0–100). | [optional] 
**Cpc** | **decimal** | Cost per click in native currency. | [optional] 
**Cpm** | **decimal** | Cost per 1000 impressions in native currency. | [optional] 
**Conversions** | **int** | Sum of conversion events over the range. Meta: events matching the campaign optimization goal. Google: tracked conversions. X / LinkedIn: reported website/lead conversions (added 2026-07). | [optional] 
**CostPerConversion** | **decimal** |  | [optional] 
**Actions** | **Dictionary&lt;string, decimal&gt;** | Per-action-type counts merged across all ads on this day. Keys are platform-native action types. | [optional] 
**ActionValues** | **Dictionary&lt;string, decimal&gt;** | Monetary mirror of &#x60;actions&#x60; in native currency. | [optional] 
**PurchaseValue** | **decimal** | Sum of purchase-type action values on this day, native currency. | [optional] 
**Roas** | **decimal** | Derived purchaseValue / spend. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

