# Zernio.Model.GetAllAccountsHealth200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Username** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**CanPost** | **bool** |  | [optional] 
**CanFetchAnalytics** | **bool** |  | [optional] 
**AnalyticsSupported** | **bool** | Whether analytics is in scope for this account at all (the platform offers analytics and it was requested at connect). False means canFetchAnalytics is not a problem to fix; true with canFetchAnalytics false means analytics needs a reconnect. | [optional] 
**ScopeAreas** | **Dictionary&lt;string, GetAllAccountsHealth200ResponseAccountsInner.InnerEnum&gt;** | Present when the account connected with &#x60;scopes&#x60; or through your own OAuth app: each permission area the platform splits, as granted, missing or not_requested. An area never requested does not make the account unhealthy. | [optional] 
**TokenValid** | **bool** |  | [optional] 
**TokenExpiresAt** | **DateTime** |  | [optional] 
**NeedsReconnect** | **bool** | True when the token is expired or revoked, permissions are missing, the account is inactive, or the platform rejected its stored credentials (the same flag the account listing reports as needsReconnection). | [optional] 
**Issues** | **List&lt;string&gt;** |  | [optional] 
**OwnerUserId** | **string** | User id of the profile owner, not necessarily the team member who connected the account. | [optional] 
**DisconnectReason** | **string** | Why the connection is broken or its token refresh is failing, from the most recent current cause. Null when the connection is healthy, including when the account is unhealthy for another reason (analytics, messaging restriction, missing analytics scopes), or when no cause is stored. | [optional] 
**DisconnectionType** | **string** | intentional: deliberately disconnected by the user or by Zernio (for example a plan downgrade), not a token failure. unintentional: token expired or revoked, or an auth failure. Null when disconnectReason is null. | [optional] 
**UnhealthySince** | **DateTime?** | When the earliest current stored cause was recorded (the start of the outage); for an intentional disconnect, when it was disconnected. Null when the connection is healthy, including when the account is unhealthy for another reason (analytics, messaging restriction, missing analytics scopes), or when the time is unknown. | [optional] 
**AnalyticsSync** | [**GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync**](GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync.md) |  | [optional] 
**InboundActivity** | [**InboundActivity**](InboundActivity.md) |  | [optional] 
**MessagingRestriction** | [**GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction**](GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

