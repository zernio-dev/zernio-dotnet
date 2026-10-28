# Zernio.Model.SettleCampaignParticipantRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AmountCents** | **int** | Defaults to the whole payable balance. | [optional] 
**ExternalReference** | **string** | Your payout id. Required when the campaign settles externally. | [optional] 
**RecordOnly** | **bool** | Treasury campaigns only: record a payout you already made outside Zernio, without moving money. Ignored on other settlement modes, which always record. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

