# Zernio.Model.UsageMetering
Billed spend by product family over a window, from Metronome's invoice breakdown (the CHARGE view). Returned by `GET /v1/usage`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Supported** | **bool** | False for legacy Stripe accounts (no Metronome invoice to split); &#x60;days&#x60; and &#x60;totals&#x60; are then empty/zero. | [optional] 
**Granularity** | **string** |  | [optional] 
**Days** | [**List&lt;UsageMeteringDaysInner&gt;**](UsageMeteringDaysInner.md) | One row per bucket. Empty when &#x60;granularity&#x3D;total&#x60;. &#x60;date&#x60; is a UTC date (month buckets use the 1st). | [optional] 
**Totals** | [**UsageMeteringTotals**](UsageMeteringTotals.md) |  | [optional] 
**LineItems** | [**List&lt;UsageMeteringLineItemsInner&gt;**](UsageMeteringLineItemsInner.md) | Per-invoice-line-item rows (largest spend first) for a detailed breakdown. | [optional] 
**Peaks** | [**UsageMeteringPeaks**](UsageMeteringPeaks.md) |  | [optional] 
**CallUsage** | [**UsageMeteringCallUsage**](UsageMeteringCallUsage.md) |  | [optional] 
**Period** | [**UsageMeteringPeriod**](UsageMeteringPeriod.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

