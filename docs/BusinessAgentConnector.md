# Zernio.Model.BusinessAgentConnector
Secret values are never returned: auth_config and mtls_config leave out client_secret, client_key, private_key and every API key value. Send them again with the credentials call to rotate them.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**BaseUrl** | **string** |  | 
**ConnectorProtocol** | **string** |  | [optional] 
**AuthType** | **string** |  | 
**AuthConfig** | **Dictionary&lt;string, Object&gt;** | What Meta stores for the connector&#39;s auth (for example oauth2_client_credentials with token_url and client_id), without secret values. | [optional] 
**UserAuthInjectionConfig** | [**BusinessAgentConnectorUserAuthInjectionConfig**](BusinessAgentConnectorUserAuthInjectionConfig.md) |  | [optional] 
**RequiresCertificate** | **bool** |  | [optional] 
**McpToolSync** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**MtlsConfig** | **Dictionary&lt;string, Object&gt;** | Certificate details, without client_key or private_key. | [optional] 
**ConnectionStatus** | [**BusinessAgentConnectorConnectionStatus**](BusinessAgentConnectorConnectionStatus.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

