# Zernio.Model.UpdateAutoRechargeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Turns auto top-up on or off. A rule switched off by failed charges stays off until the card is updated. | [optional] 
**BelowCents** | **int** | Auto top-up charges the card when the balance drops below this, in cents. At least $5. | [optional] 
**ToCents** | **int** | Top back up to this, in cents. More than $5 above belowCents. | [optional] 
**MonthlyLimitCents** | **int?** | Most auto top-up may add per calendar month (UTC), before tax. At least toCents while auto top-up is on. Null for no limit. | [optional] 
**AlertBelowCents** | **int?** | Email the billing owner once each time the balance drops below this. Null for no email. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

