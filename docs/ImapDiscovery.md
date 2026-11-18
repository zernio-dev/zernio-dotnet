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
**UnsupportedReason** | **string** | Why an &#x60;unsupported&#x60; route cannot connect:  - &#x60;proton_requires_bridge&#x60;: Proton Mail only works through its local bridge. - &#x60;forwarding_only&#x60;: the domain forwards mail (Cloudflare Email Routing) and stores none, so connect the mailbox it forwards to. - &#x60;domain_typo&#x60;: the domain takes no mail and looks like a mistyped consumer domain. &#x60;suggestedEmail&#x60; has the likely address. - &#x60;no_mail_domain&#x60;: the domain has no MX and no address, so it cannot receive email.  | [optional] 
**SuggestedEmail** | **string** | With unsupportedReason domain_typo: the address the user most likely meant, such as ana7275@gmail.com for ana@7275gmail.com. Run discovery again with it once the user confirms. | [optional] 
**AppPasswordFallback** | **Object** | Google only: Gmail over IMAP with an app password, for accounts whose admin blocks Google sign-in for other apps. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

