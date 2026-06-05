# Zernio.Model.AdjustConversionsRequestAdjustmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdjustmentType** | **string** |  | 
**AdjustmentTime** | **decimal** | When the adjustment occurred, unix seconds. | 
**OrderId** | **string** | Transaction ID of the original conversion (the &#x60;eventId&#x60; you sent). Recommended; required for ENHANCEMENT. | [optional] 
**Gclid** | **string** | Alternative key — the original click ID. Pair with &#x60;conversionTime&#x60;. Not valid for ENHANCEMENT. | [optional] 
**ConversionTime** | **decimal** | The original conversion&#39;s time, unix seconds. Required when identifying by &#x60;gclid&#x60;. | [optional] 
**RestatementValue** | **decimal** | RESTATEMENT only — the corrected TOTAL conversion value. | [optional] 
**Currency** | **string** | RESTATEMENT only — ISO 4217 currency for &#x60;restatementValue&#x60;. | [optional] 
**User** | [**AdjustConversionsRequestAdjustmentsInnerUser**](AdjustConversionsRequestAdjustmentsInnerUser.md) |  | [optional] 
**UserAgent** | **string** | ENHANCEMENT only — the original conversion&#39;s user agent (improves match quality). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

