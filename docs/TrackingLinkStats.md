# Zernio.Model.TrackingLinkStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromDate** | **DateOnly** |  | 
**ToDate** | **DateOnly** |  | 
**Clicks** | **int** | Human clicks in the range. | 
**Conversions** | **int** | Conversions still counted whose time falls in the range. | 
**ConversionRate** | **decimal?** | Conversions per click. Null without clicks. | 
**Revenue** | [**List&lt;TrackingLinkStatsRevenueInner&gt;**](TrackingLinkStatsRevenueInner.md) | The conversions&#39; value summed per currency, most conversions first. | 
**Destinations** | [**List&lt;TrackingLinkStatsDestinationsInner&gt;**](TrackingLinkStatsDestinationsInner.md) | The link&#39;s current destinations, each with its clicks in the range. | 
**FormerDestinationClicks** | **int** | Clicks on destinations the link no longer has (an edited or removed URL). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

