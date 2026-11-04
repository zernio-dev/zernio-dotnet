# Zernio.Model.WebhookPayloadAccountDisconnectedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | The account&#39;s unique identifier (same as used in /v1/accounts/{accountId}) | 
**ProfileId** | **string** | The profile&#39;s unique identifier this account belongs to | 
**Platform** | **string** |  | 
**Username** | **string** |  | 
**DisplayName** | **string** |  | [optional] 
**DisconnectionType** | **string** | intentional: removed on purpose, for example with DELETE /v1/accounts/{accountId} or by a switch to the Free plan for the accounts over its limit. The account is deleted permanently 1 hour later unless the same account is reconnected within that hour.  unintentional: the connection broke (token expired or revoked, access lost on the platform). The account stays in Zernio, inactive, until it is reconnected (keeping its accountId) or removed. | 
**Reason** | **string** | Human-readable reason for the disconnection | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

