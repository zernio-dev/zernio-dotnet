# Zernio.Model.InstallTrackingTagOnStore200ResponseInstall

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StoreAccountId** | **string** |  | [optional] 
**Platform** | **string** | The store platform. | [optional] 
**TagPlatform** | **string** | Platform of the tag this install is about (e.g. &#x60;metaads&#x60;). | [optional] 
**SiteTagId** | **string** | The id the tag carries on the site (see &#x60;TrackingTag.siteTagId&#x60;). | [optional] 
**Installed** | **bool** | Shopify: this tag is the one the store fires for its platform. WordPress: the Zernio widget for this tag is in an active widget area with its script intact. | [optional] 
**ShopDomain** | **string** | Shopify only. | [optional] 
**InstalledTagId** | **string** | Shopify only: the tag of the same platform the store fires now (may be a different tag), or null. | [optional] 
**Tags** | [**List&lt;StorePixelInstallTagsInner&gt;**](StorePixelInstallTagsInner.md) | GET only on WordPress, always on Shopify: every Zernio tag on the store, all platforms. | [optional] 
**WebPixelId** | **string** | Shopify only: web pixel id, or null when nothing is installed. | [optional] 
**SiteUrl** | **string** | WordPress only. | [optional] 
**Method** | **string** | WordPress only. | [optional] 
**WidgetId** | **string** | WordPress only: widget id, e.g. &#x60;custom_html-3&#x60;. | [optional] 
**SidebarId** | **string** | WordPress only: widget area holding the widget. | [optional] 
**ReplacedTagId** | **string** | Shopify only: the pixel this install replaced on the store, if any. | [optional] 
**SidebarName** | **string** | WordPress only: name of the widget area used. | [optional] 
**Created** | **bool** | WordPress only: false when an existing Zernio widget was updated. | [optional] 
**HomepageCheck** | **string** | WordPress only: whether the pixel appeared in the homepage HTML. &#x60;not_found&#x60; can be a stale page cache. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

