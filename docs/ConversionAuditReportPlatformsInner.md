# Zernio.Model.ConversionAuditReportPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** | Stable platform key (meta, google, tiktok, ...). | 
**Name** | **string** | Human-readable platform name. | 
**BrowserPixel** | **bool** | Whether a browser pixel for this platform was found. | 
**ServerSide** | **bool** | True only when a server-side path is proven: visible from the page, or verified through the Zernio account behind the site tag. | 
**RelayedBy** | **string** | The only server path seen is the Zernio site tag relay; &#x60;serverSideVerified&#x60; says whether its delivery to this platform is proven. | [optional] 
**ServerSideVerified** | **bool** | The Zernio site tag on the page belongs to an account whose destination for this platform accepted the site&#39;s events in the last 7 days. | [optional] 
**ServerTool** | **string** | A third-party server-side tool installed on the site that may already send this platform&#39;s events (Elevar, Littledata, Stape), when its status is &#x60;likely&#x60;. Which platforms the tool feeds is not visible from the page. | [optional] 
**Status** | **string** | &#x60;good&#x60; &#x3D; server-side, &#x60;warn&#x60; &#x3D; browser-only (the leak), &#x60;missing&#x60; &#x3D; not tracked, &#x60;not-firing&#x60; &#x3D; the tag is installed but sent nothing during a full visit. | 
**EstimatedLossBrowserOnly** | **decimal** | Share of conversions typically lost when this platform runs browser-only, 0-1. | 
**Note** | **string** | Short explanation of the finding. | 
**Ids** | **List&lt;string&gt;** | Pixel or tag ids found for this platform. | [optional] 
**Events** | **List&lt;string&gt;** | Standard events called in the page or its tag-manager containers. | [optional] 
**FixSteps** | **List&lt;string&gt;** | Steps to fix this platform&#39;s tracking. | [optional] 
**Fired** | **string** | Rendered scans: &#x60;after-consent&#x60; when the pixel fired only once the scan accepted the cookie banner. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

