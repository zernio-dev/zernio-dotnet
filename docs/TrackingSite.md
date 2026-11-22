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
**GoogleTagIds** | **List&lt;string&gt;** | The site&#39;s own Google tags (Tag Manager, GA4, Google Ads) its own-domain path relays to Google, so they load and measure from the site&#39;s domain. | [optional] 
**ConsentMode** | **TrackingSiteConsentMode** |  | [optional] 
**Pixels** | [**List&lt;TrackingSitePixel&gt;**](TrackingSitePixel.md) | The ad pixels the tag loads itself. In the EEA, UK and Switzerland none loads before the visitor accepts on the site&#39;s consent banner; elsewhere &#x60;consentMode&#x60; decides. | [optional] 
**ConsentModeBridge** | **bool** | The tag writes the answer on the site&#39;s consent banner into Google Consent Mode v2: denied by default in the EEA, UK and Switzerland, then updated. On for sites created from November 2026. | [optional] 
**Checks** | [**List&lt;TrackingSiteChecksInner&gt;**](TrackingSiteChecksInner.md) | One per setup step: &#x60;script&#x60; for the install, then one per ad account the site sends to, keyed by its platform and ids. | [optional] 
**Setup** | [**TrackingSiteSetup**](TrackingSiteSetup.md) |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

