# Zernio.Model.CreatorPortalReferral

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **string** | The creator&#39;s discount code. Null while the store has not created it yet, or on a link-only campaign. | 
**DiscountPercent** | **int?** | What the code takes off an order. | 
**TrackingUrl** | **string** | The landing page with the UTM parameters that credit the creator. Null on a code-only campaign. | 
**Orders** | [**List&lt;CreatorPortalReferralOrdersInner&gt;**](CreatorPortalReferralOrdersInner.md) | The latest 50 credited orders. | 
**Totals** | [**CreatorPortalReferralTotals**](CreatorPortalReferralTotals.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

