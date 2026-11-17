# Zernio.Model.TrackingSite

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Install** | [**TrackingSiteInstall**](TrackingSiteInstall.md) |  | [optional] 
**StoreOrders** | **bool** | True when the store&#39;s orders reach Zernio from the store itself, so website purchases are forwarded but not counted twice. | [optional] 
**SiteKey** | **string** | Public key that names the site in the snippet, such as &#x60;zs_...&#x60;. | [optional] 
**Domains** | **List&lt;string&gt;** |  | [optional] 
**CustomHostname** | [**TrackingSiteCustomHostname**](TrackingSiteCustomHostname.md) |  | [optional] 
**Proxy** | [**TrackingSiteProxy**](TrackingSiteProxy.md) |  | [optional] 
**ConsentMode** | **TrackingSiteConsentMode** |  | [optional] 
**Checks** | [**List&lt;TrackingSiteChecksInner&gt;**](TrackingSiteChecksInner.md) | One per setup step: &#x60;script&#x60; for the install, then one per ad account the site sends to, keyed by its platform and ids. | [optional] 
**Setup** | [**TrackingSiteSetup**](TrackingSiteSetup.md) |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

