# Zernio.Model.ListLedgerEntries200ResponseEntriesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Kind** | **string** |  | [optional] 
**AmountCents** | **int** | Always positive; direction is given by debit and credit | [optional] 
**Debit** | [**LedgerAccountSide**](LedgerAccountSide.md) |  | [optional] 
**Credit** | [**LedgerAccountSide**](LedgerAccountSide.md) |  | [optional] 
**HoldUntil** | **DateTime?** |  | [optional] 
**ReleasedByEntryId** | **string** |  | [optional] 
**ReferenceType** | **string** |  | [optional] 
**ReferenceId** | **string** |  | [optional] 
**ReversesEntryId** | **string** |  | [optional] 
**Cause** | **string** |  | [optional] 
**Actor** | **string** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

