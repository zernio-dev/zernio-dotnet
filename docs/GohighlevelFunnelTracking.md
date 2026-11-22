# Zernio.Model.GohighlevelFunnelTracking

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SiteId** | **string** | The Zernio tracking site behind the tag (&#x60;getTrackingSite&#x60;). | 
**Snippet** | **string** | The line to paste into each funnel&#39;s and website&#39;s tracking code (Header). | 
**Live** | **bool** | The tag has sent its first visit. | 
**Domains** | **List&lt;string&gt;** | The domains whose visits are tied to contacts. A page checked with &#x60;verifyGohighlevelFunnelTracking&#x60; adds its domain. | 
**Funnels** | [**List&lt;GohighlevelFunnelTrackingFunnelsInner&gt;**](GohighlevelFunnelTrackingFunnelsInner.md) |  | 
**Verified** | [**GohighlevelFunnelTrackingVerified**](GohighlevelFunnelTrackingVerified.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

