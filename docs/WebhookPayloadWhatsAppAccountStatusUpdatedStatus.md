# Zernio.Model.WebhookPayloadWhatsAppAccountStatusUpdatedStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** | &#x60;active&#x60; only on a reinstatement (DISABLED_UPDATE with ban state REINSTATE). | 
**MetaEvent** | **string** | Meta &#x60;account_update&#x60; event: ACCOUNT_RESTRICTION, ACCOUNT_VIOLATION, ACCOUNT_DELETED or DISABLED_UPDATE. | 
**Reason** | **string** | Human-readable summary. Null on reinstatement. | 
**ViolationType** | **string** | ACCOUNT_VIOLATION only, for example SCAM, ADULT. | 
**Restrictions** | [**List&lt;WebhookPayloadWhatsAppAccountStatusUpdatedStatusRestrictionsInner&gt;**](WebhookPayloadWhatsAppAccountStatusUpdatedStatusRestrictionsInner.md) | ACCOUNT_RESTRICTION only. Empty otherwise. | 
**BanState** | **string** | DISABLED_UPDATE only (for example DISABLE, REINSTATE). | 
**BanDate** | **string** | DISABLED_UPDATE only, as Meta sent it (for example \&quot;September 23, 2026\&quot;). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

