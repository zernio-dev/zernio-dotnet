# Zernio.Model.CreateTopupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AmountCents** | **int** | Amount in cents, minimum $10 | 
**Method** | **string** | Only card is available. bank_transfer returns 400 \&quot;Bank transfers are not available yet.\&quot; | 
**PaymentMethodId** | **string** | A saved card of the billing owner&#39;s (&#x60;pm_...&#x60;). Defaults to the default payment method. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

