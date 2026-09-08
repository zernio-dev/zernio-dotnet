# Zernio.Model.BusinessAgentConnector

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Unique per number. | 
**Description** | **string** | Tell the agent what the service provides. | [optional] 
**BaseUrl** | **string** | Public HTTPS URL reachable from Meta. | 
**ConnectorProtocol** | **string** |  | [optional] 
**AuthType** | **string** |  | 
**AuthConfig** | [**BusinessAgentConnectorInputAuthConfig**](BusinessAgentConnectorInputAuthConfig.md) |  | [optional] 
**UserAuthInjectionConfig** | [**BusinessAgentConnectorInputUserAuthInjectionConfig**](BusinessAgentConnectorInputUserAuthInjectionConfig.md) |  | [optional] 
**RequiresCertificate** | **bool** |  | [optional] 
**Id** | **string** |  | 
**McpToolSync** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**MtlsConfig** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**ConnectionStatus** | [**BusinessAgentConnectorAllOfConnectionStatus**](BusinessAgentConnectorAllOfConnectionStatus.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

