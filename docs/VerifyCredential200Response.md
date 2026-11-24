# Zernio.Model.VerifyCredential200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Valid** | **bool** |  | [optional] 
**UserId** | **string** |  | [optional] 
**Name** | **string** | Display name of the credential&#39;s owner. | [optional] 
**Email** | **string** | Email of the credential&#39;s owner. | [optional] 
**AuthType** | **string** |  | [optional] 
**Scope** | **string** | Granted OAuth scopes, space-separated. Null for API keys. | [optional] 
**Audience** | **string** | Resource the OAuth token was issued for (RFC 8707), for example https://mcp.zernio.com/mcp. Null for API keys and for tokens issued without one. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

