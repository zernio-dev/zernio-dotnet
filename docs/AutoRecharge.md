# Zernio.Model.AutoRecharge

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Whether auto top-up is on. Charges happen only when this is true and disabledReason is null. | 
**BelowCents** | **int** | Top up when the balance drops below this, in cents. | 
**ToCents** | **int** | Top back up to this, in cents. The charge is toCents minus the balance, plus tax. | 
**MonthlyLimitCents** | **int?** | Most auto top-up may add per calendar month (UTC), before tax; null for no limit. | 
**AlertBelowCents** | **int?** | Low-balance email threshold, sent once per drop below it; null for none. | 
**DisabledReason** | **string** | &#x60;payment_failed&#x60; after four failed charges in a row. Updating the card clears it. | 
**RetryCount** | **int** | Failed charges in a row; 0 once one goes through. | 
**NextRetryAt** | **DateTime?** | When a declined auto top-up is tried again; null when none is waiting. | 
**MonthRechargedCents** | **int** | Auto top-ups this calendar month (UTC), paid or being paid, before tax. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

