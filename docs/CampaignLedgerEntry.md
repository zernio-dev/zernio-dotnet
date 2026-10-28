# Zernio.Model.CampaignLedgerEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Kind** | **string** |  | 
**AmountCents** | **int** | Always positive; direction is given by debit and credit. | 
**Debit** | [**LedgerAccountSide**](LedgerAccountSide.md) |  | 
**Credit** | [**LedgerAccountSide**](LedgerAccountSide.md) |  | 
**HoldUntil** | **DateTime?** |  | 
**ReleasedByEntryId** | **string** |  | 
**ReversesEntryId** | **string** |  | 
**ReferenceType** | **string** |  | 
**ReferenceId** | **string** |  | 
**Cause** | **string** |  | 
**ExternalReference** | **string** | The payout reference recorded with a settlement (your transfer or invoice id). | 
**Actor** | **string** |  | 
**CreatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

