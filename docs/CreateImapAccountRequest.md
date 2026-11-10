# Zernio.Model.CreateImapAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**Email** | **string** |  | 
**Name** | **string** | Shown to people the mailbox emails. | [optional] 
**Password** | **string** | Shortcut for imap.password. | [optional] 
**Imap** | [**CreateImapAccountRequestImap**](CreateImapAccountRequestImap.md) |  | [optional] 
**Smtp** | [**CreateImapAccountRequestSmtp**](CreateImapAccountRequestSmtp.md) |  | [optional] 
**Identities** | [**List&lt;CreateImapAccountRequestIdentitiesInner&gt;**](CreateImapAccountRequestIdentitiesInner.md) | Other addresses this mailbox sends as. | [optional] 
**DryRun** | **bool** | Run every check and store nothing, for live validation in your own form. | [optional] 
**AllowSelfSignedCertificate** | **bool** | On-premise servers only: accept a certificate that cannot be verified. The hosted page never offers it. | [optional] 
**ReconnectAccountId** | **string** | Reconnect this account in place with a new password; the stored servers are reused. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

