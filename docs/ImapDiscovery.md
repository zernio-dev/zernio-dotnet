# Zernio.Model.ImapDiscovery

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **string** |  | [optional] 
**Route** | **string** |  | [optional] 
**Provider** | [**ImapDiscoveryProvider**](ImapDiscoveryProvider.md) |  | [optional] 
**Source** | **string** |  | [optional] 
**Confidence** | **string** | low when only a probe answered: show the settings for the user to check. | [optional] 
**Imap** | [**ImapDiscoveryImap**](ImapDiscoveryImap.md) |  | [optional] 
**Smtp** | [**ImapDiscoverySmtp**](ImapDiscoverySmtp.md) |  | [optional] 
**Auth** | [**ImapDiscoveryAuth**](ImapDiscoveryAuth.md) |  | [optional] 
**Preflight** | [**List&lt;ImapDiscoveryPreflightInner&gt;**](ImapDiscoveryPreflightInner.md) | What to switch on at the provider first, such as IMAP access on GMX or Yandex. | [optional] 
**ReconnectCause** | **string** |  | [optional] 
**Reason** | **string** |  | [optional] 
**UnsupportedReason** | **string** |  | [optional] 
**AppPasswordFallback** | **Object** | Google only: Gmail over IMAP with an app password, for accounts whose admin blocks Google sign-in for other apps. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

