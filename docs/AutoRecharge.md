# Zernio.Model.AutoRecharge

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Whether auto top-up is on. Charges happen only when this is true and disabledReason is null. | 
**BelowCents** | **int** | The below amount, in cents: when the balance drops below this, auto top-up brings it back to toCents. | 
**ToCents** | **int** | The back-to amount, in cents. The charge is toCents minus the balance (at least $5, at most toCents unless the balance is below $0 or a monthly fee is due), plus tax. | 
**MonthlyLimitCents** | **int?** | Most auto top-up may add per calendar month (UTC), before tax; null for no limit. | 
**AlertBelowCents** | **int?** | Low-balance email threshold, sent once per drop below it; null for none. | 
**DisabledReason** | **string** | &#x60;payment_failed&#x60; once a declined charge is not retried, or its one retry fails; updating the card clears it. &#x60;charge_error&#x60; after 24 charges in a row failed on our side (not the card); turning auto top-up back on (&#x60;enabled: true&#x60;) clears it. | 
**RetryCount** | **int** | Failed charges in a row; 0 once one goes through. | 
**NextRetryAt** | **DateTime?** | When a declined auto top-up is tried again; null when none is waiting. | 
**MonthRechargedCents** | **int** | Auto top-ups this calendar month (UTC), paid or being paid, before tax. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

