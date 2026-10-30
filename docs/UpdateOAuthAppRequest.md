# Zernio.Model.UpdateOAuthAppRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Label** | **string** |  | [optional] 
**ClientSecret** | **string** |  | [optional] 
**MetaAppId** | **string** | Instagram only: the numeric ID of the Meta app your Instagram app lives in. Zernio uses it with &#x60;metaAppSecret&#x60; to register the webhook. Send both or neither. | [optional] 
**MetaAppSecret** | **string** | Instagram only: the secret of that Meta app. Never returned. | [optional] 
**SlackSigningSecret** | **string** | Slack only: saves or replaces the signing secret from the app&#39;s Basic Information page; any other platform is a 400. | [optional] 
**ScopeAreas** | **List&lt;UpdateOAuthAppRequest.ScopeAreasEnum&gt;** | Replaces the areas new connects request. Accounts already connected keep what they were granted until they reconnect. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

