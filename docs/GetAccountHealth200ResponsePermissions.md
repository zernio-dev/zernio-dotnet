# Zernio.Model.GetAccountHealth200ResponsePermissions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Posting** | [**List&lt;GetAccountHealth200ResponsePermissionsPostingInner&gt;**](GetAccountHealth200ResponsePermissionsPostingInner.md) |  | [optional] 
**Analytics** | [**List&lt;GetAccountHealth200ResponsePermissionsPostingInner&gt;**](GetAccountHealth200ResponsePermissionsPostingInner.md) |  | [optional] 
**Optional** | [**List&lt;GetAccountHealth200ResponsePermissionsPostingInner&gt;**](GetAccountHealth200ResponsePermissionsPostingInner.md) |  | [optional] 
**CanPost** | **bool** | Whether the granted OAuth scopes allow posting. Scopes only: for WhatsApp, whether Meta lets the number send is &#x60;platformConnection.phoneStatus&#x60; and the overall &#x60;status&#x60;. | [optional] 
**CanFetchAnalytics** | **bool** |  | [optional] 
**AnalyticsSupported** | **bool** | Whether analytics is in scope for this account at all (the platform offers analytics and it was requested at connect). False means canFetchAnalytics is not a problem to fix; true with canFetchAnalytics false means analytics needs a reconnect. | [optional] 
**MissingRequired** | **List&lt;string&gt;** |  | [optional] 
**ScopeAreas** | **Dictionary&lt;string, GetAccountHealth200ResponsePermissions.InnerEnum&gt;** | Present when the account connected with &#x60;scopes&#x60; or through your own OAuth app: each permission area the platform splits, as granted, missing or not_requested. An area never requested does not make the account unhealthy. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

