# Zernio.Model.TreasuryTransfer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**PayeeId** | **string** | 24-character payee id | [optional] 
**PayeeName** | **string** | The payee&#39;s name when Zernio knows it, for example a creator&#39;s display name in one of your creator campaigns; null otherwise | [optional] 
**DestinationType** | **string** |  | [optional] 
**AmountCents** | **int** | Amount the payee receives, in full | [optional] 
**FeeCents** | **int** | Zernio fee added on top, 4% with a 50 cent minimum | [optional] 
**TotalCents** | **int** | Amount debited from your balance: amountCents plus feeCents | [optional] 
**Currency** | **string** |  | [optional] 
**Reference** | [**TreasuryTransferReference**](TreasuryTransferReference.md) |  | [optional] 
**Status** | **string** |  | [optional] 
**FailureReason** | **string** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

