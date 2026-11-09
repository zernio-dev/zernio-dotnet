# Zernio.Model.WebhookPayloadBalanceChargedTopup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The top-up id, as in GET /v1/balance (&#x60;recentTopups&#x60;) and its invoice and receipt endpoints. | 
**Trigger** | **string** | &#x60;manual&#x60;: someone added funds in Billing or through the API. &#x60;auto_top_up&#x60;: the auto top-up rule charged the card. | 
**AmountCents** | **int** | Added to the balance, in USD cents. | 
**TaxCents** | **int** | VAT charged on top, in USD cents (0 when none applies). | 
**ChargedCents** | **int** | What the card was charged, in USD cents: amount plus tax. | 
**Currency** | **string** |  | 
**Card** | [**WebhookPayloadBalanceChargedTopupCard**](WebhookPayloadBalanceChargedTopupCard.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

