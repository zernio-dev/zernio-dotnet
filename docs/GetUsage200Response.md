# Zernio.Model.GetUsage200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillingSystem** | **string** | Which billing system the account is on. Shape of &#x60;usage&#x60;/&#x60;spend&#x60; differs. | [optional] 
**PlanName** | **string** |  | [optional] 
**BillingPeriod** | **string** |  | [optional] 
**SignupDate** | **DateTime** |  | [optional] 
**BillingAnchorDay** | **int** | Day of month (1-31) when the billing cycle resets | [optional] 
**HasAccess** | **bool** | True if the account is in good standing. False for past-due/unpaid/paused subscriptions. | [optional] 
**CustomerId** | **string** | Stripe customer ID, when present. | [optional] 
**IsInvitedUser** | **bool** | True if this is a team member; limits/usage reflect the account owner. | [optional] 
**AutoUpgradeEnabled** | **bool** | Stripe-only. Always false for Metronome users. | [optional] 
**Limits** | [**UsageStatsLimits**](UsageStatsLimits.md) |  | [optional] 
**Usage** | [**UsageStatsUsage**](UsageStatsUsage.md) |  | [optional] 
**Spend** | [**UsageStatsSpend**](UsageStatsSpend.md) |  | [optional] 
**Supported** | **bool** | False for legacy Stripe accounts (no Metronome invoice to split); &#x60;days&#x60; and &#x60;totals&#x60; are then empty/zero. | [optional] 
**Granularity** | **string** |  | [optional] 
**Days** | [**List&lt;UsageMeteringDaysInner&gt;**](UsageMeteringDaysInner.md) | One row per bucket. Empty when &#x60;granularity&#x3D;total&#x60;. &#x60;date&#x60; is a UTC date (month buckets use the 1st). | [optional] 
**Totals** | [**UsageMeteringTotals**](UsageMeteringTotals.md) |  | [optional] 
**LineItems** | [**List&lt;UsageMeteringLineItemsInner&gt;**](UsageMeteringLineItemsInner.md) | Per-invoice-line-item rows (largest spend first) for a detailed breakdown. | [optional] 
**Peaks** | [**UsageMeteringPeaks**](UsageMeteringPeaks.md) |  | [optional] 
**CallUsage** | [**UsageMeteringCallUsage**](UsageMeteringCallUsage.md) |  | [optional] 
**Period** | [**UsageMeteringPeriod**](UsageMeteringPeriod.md) |  | [optional] 
**Tax** | [**UsageMeteringTax**](UsageMeteringTax.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

