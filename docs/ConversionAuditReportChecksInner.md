# Zernio.Model.ConversionAuditReportChecksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable check id, such as &#x60;pixels&#x60;, &#x60;server-side&#x60;, &#x60;first-party&#x60;, &#x60;consent&#x60;, &#x60;consent-timing&#x60; or &#x60;match-quality&#x60;. New checks can appear. | 
**Title** | **string** |  | 
**Status** | **string** | &#x60;unknown&#x60; &#x3D; the scan cannot see it from outside; &#x60;not-applicable&#x60; checks are left out of the score. | 
**Tier** | **string** | A &#x60;bonus&#x60; check can only add points, never cost them. | [optional] 
**Weight** | **decimal** |  | 
**Detail** | **string** |  | 
**PointsToGain** | **decimal** | Points the score gains when this check alone is fixed. | [optional] 
**Verify** | [**ConversionAuditReportChecksInnerVerify**](ConversionAuditReportChecksInnerVerify.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

