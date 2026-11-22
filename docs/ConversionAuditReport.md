# Zernio.Model.ConversionAuditReport
The scored conversion-tracking audit of one page.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Url** | **string** | The normalized URL that was scanned. | 
**Domain** | **string** | The scanned host without &#x60;www.&#x60;. | 
**Score** | **decimal** | Conversion tracking score, 0-100. Higher means a more complete setup and less signal at risk. | 
**Grade** | **string** | Letter grade for the score. | 
**ScoreRange** | [**ConversionAuditReportScoreRange**](ConversionAuditReportScoreRange.md) |  | [optional] 
**EstimatedSignalLossPct** | **decimal** | Average share of conversions at risk on the networks with no visible server-side path, 0-100. | 
**Platforms** | [**List&lt;ConversionAuditReportPlatformsInner&gt;**](ConversionAuditReportPlatformsInner.md) | One finding per ad platform the scan looked for. | 
**BrowserOnly** | **bool** | True when every active platform is tracked browser-only. | 
**ConsentManager** | **string** | Consent manager found on the page, or null. | 
**ActivePlatformCount** | **int** | How many ad platforms the scan found any tracking for. | 
**Visibility** | **string** | &#x60;full&#x60; &#x3D; pixels were visible, &#x60;limited&#x60; &#x3D; tags load dynamically so not all are visible, &#x60;none&#x60; &#x3D; nothing found. | 
**SiteSignals** | **List&lt;string&gt;** | Site tech recognized (Shopify, WooCommerce, ...). | 
**ScanMode** | **string** | &#x60;rendered&#x60; when a headless browser ran the page and its requests were checked, &#x60;static&#x60; for the page source only. | [optional] 
**Limitations** | **List&lt;string&gt;** | What this scan could not see. | [optional] 
**Checks** | [**List&lt;ConversionAuditReportChecksInner&gt;**](ConversionAuditReportChecksInner.md) | The scored checks behind &#x60;score&#x60;. | [optional] 
**ServerSide** | [**ConversionAuditReportServerSide**](ConversionAuditReportServerSide.md) |  | [optional] 
**Consent** | [**ConversionAuditReportConsent**](ConversionAuditReportConsent.md) |  | [optional] 
**ConsentScan** | [**ConversionAuditReportConsentScan**](ConversionAuditReportConsentScan.md) |  | [optional] 
**TagManagers** | **List&lt;string&gt;** |  | [optional] 
**OtherNetworks** | [**List&lt;ConversionAuditReportOtherNetworksInner&gt;**](ConversionAuditReportOtherNetworksInner.md) | Ad networks found that the score does not cover. &#x60;relaySupported&#x60; is true when Zernio can send them conversions. | [optional] 
**OtherNetworksConfigured** | [**List&lt;ConversionAuditReportOtherNetworksInner&gt;**](ConversionAuditReportOtherNetworksInner.md) | Rendered scans: unscored ad networks found only in a Google Tag Manager container that the visit never saw load or send. Not counted in &#x60;otherNetworks&#x60;. | [optional] 
**FaviconUrl** | **string** | The site&#39;s icon. Absent when the site was unreachable. | [optional] 
**Summary** | **string** | One-paragraph summary of the audit. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

