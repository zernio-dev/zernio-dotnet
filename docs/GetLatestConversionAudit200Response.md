# Zernio.Model.GetLatestConversionAudit200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Report** | [**ConversionAuditReport**](ConversionAuditReport.md) |  | 
**Networks** | [**List&lt;ConversionAuditAnswerNetworksInner&gt;**](ConversionAuditAnswerNetworksInner.md) | Each ad network with its final setup and leak, computed exactly as the public report page shows them, best setup first. Empty when &#x60;report.scannerBlocked&#x60; is set: the scan could not see any network. | 
**TopFixes** | [**List&lt;ConversionAuditAnswerTopFixesInner&gt;**](ConversionAuditAnswerTopFixesInner.md) | The few fixes that matter most, in the order the public report page lists them. | 
**FixPrompt** | **string** | A prompt to paste into a coding agent. It lists the report&#39;s findings, then connecting Zernio, sending conversions server-side and verifying them. | 
**PublicReport** | [**ConversionAuditAnswerPublicReport**](ConversionAuditAnswerPublicReport.md) |  | 
**Host** | **string** | The normalized host the report is stored under. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

