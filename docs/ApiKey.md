# Zernio.Model.ApiKey

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**KeyPreview** | **string** |  | [optional] 
**ExpiresAt** | **DateTime** |  | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**Key** | **string** | Returned only once, on creation | [optional] 
**Scope** | **string** | &#39;full&#39; grants access to all profiles, &#39;profiles&#39; restricts to specific profiles | [optional] [default to ScopeEnum.Full]
**ProfileIds** | [**List&lt;ApiKeyProfileIdsInner&gt;**](ApiKeyProfileIdsInner.md) | Profiles this key can access (populated with name and color). Only present when scope is &#39;profiles&#39;. | [optional] 
**Permission** | **string** | &#39;read-write&#39; allows all operations, &#39;read&#39; restricts to GET requests only | [optional] [default to PermissionEnum.ReadWrite]
**DisabledResourceGroups** | **List&lt;ApiKey.DisabledResourceGroupsEnum&gt;** | Resource groups this key can NOT access (opt-out denylist). Absent or empty means legacy full access. A key with any group disabled is a restricted key (zrk_ prefix) and can never manage API keys, invites, or member identity. Each operation&#39;s group is published as x-resource-group. With &#39;messages&#39; disabled, the KEY cannot access private messages; the ACCOUNT&#39;s pre-existing webhook subscriptions are a separate grant surface. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

