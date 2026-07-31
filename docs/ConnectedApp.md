# Zernio.Model.ConnectedApp
An OAuth client (AI assistant / MCP connector) authorized by the user and still holding at least one live token. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ClientId** | **string** |  | [optional] 
**ClientName** | **string** | Name the client declared at registration. Registration is open, so this is self-declared and not verified. | [optional] 
**RedirectHost** | **string** | Host of the client&#39;s registered redirect URI (non-http schemes are shown as scheme//host). The destination an impostor cannot fake. | [optional] 
**Scopes** | **List&lt;string&gt;** | Scopes granted on the most recent token. | [optional] 
**AuthorizedAt** | **DateTime?** |  | [optional] 
**LastUsedAt** | **DateTime?** | Last time any of the client&#39;s live tokens authenticated a request. | [optional] 
**TokenCount** | **int** | Live tokens held by the client (an active session is typically one access plus one refresh token). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

