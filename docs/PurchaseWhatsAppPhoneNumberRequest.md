# Zernio.Model.PurchaseWhatsAppPhoneNumberRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** | Profile to associate the number with | 
**Country** | **string** | ISO 3166-1 alpha-2 country for the number (default US). International numbers require usage-based billing. Tier 3/4 countries return 202 { status: \&quot;kyc_required\&quot;, kycUrl } — the customer must complete KYC at that URL before the number is ordered. See GET /v1/whatsapp/phone-numbers/countries.  | [optional] [default to "US"]
**PurchaseIntentId** | **string** | Optional idempotency key. Send the same value when retrying a purchase: if a number was already bought under this key, the API returns { status: \&quot;already_purchased\&quot;, numberId, phoneNumber } instead of provisioning a second number. Generate a fresh key for each genuinely new purchase.  | [optional] 
**AllowMultiple** | **bool** | Any second purchase within 10 minutes of a previous one is rejected with 409 code PURCHASE_VELOCITY as duplicate protection. Pass true to confirm the additional purchase is intentional (e.g. bulk provisioning).  | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

