# Zernio.Model.WebhookPayloadAccountConnectedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The account&#39;s unique identifier (same as used in /v1/accounts/{accountId}) | 
**ProfileId** | **string** | The profile&#39;s unique identifier this account belongs to | 
**Platform** | **string** |  | 
**Username** | **string** |  | 
**DisplayName** | **string** |  | [optional] 
**Reconnected** | **bool** | Present and true when a reconnect restored an existing account in place, keeping its accountId. | [optional] 
**ReplacedAccountId** | **string** | The IMAP account this connection replaces, when a reconnected mailbox moved to Google or Microsoft. That account is retired at the same time, with account.disconnected and reasonCode replaced. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

