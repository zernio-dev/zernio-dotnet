# Zernio.Model.InitiateWhatsAppCallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**To** | **string** | Consumer wa_id (E.164 | 
**ForwardTo** | **string** | Per-call destination override. Same accepted shape as the number&#39;s stored forwardTo (tel:+E164, sip:..., wss://...).  | [optional] 
**RecordOverride** | **bool** |  | [optional] 
**BizOpaqueCallbackData** | **string** | Accepted for forward compatibility. Not currently echoed back in webhook payloads (SIP-first flow does not pass through Meta&#39;s Graph API where Meta would echo this).  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

