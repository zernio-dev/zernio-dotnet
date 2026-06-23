# Zernio.Model.WhatsAppSandboxSession
A per-user activation session against the shared WhatsApp sandbox number. Transitions `pending → active` when the inbound webhook receives a reply from the matching phone (the reply itself proves ownership). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Session id. Use this to revoke via DELETE. | 
**PhoneE164** | **string** | Digits-only E.164 form (no +, spaces, or dashes). | 
**Status** | **string** | &#x60;pending&#x60; until the phone replies to the activation template, then &#x60;active&#x60;. Expired sessions are pruned by TTL and never appear in list responses.  | 
**ExpiresAt** | **DateTime** | UTC timestamp at which the session becomes invalid. Pending sessions get a 24h window; activated sessions get 7 days.  | 
**ActivatedAt** | **DateTime?** | When the session transitioned &#x60;pending → active&#x60;, or null. | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

