# Zernio.Model.CreateOAuthAppRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Platform** | **string** | One of the platforms listed in &#x60;platforms&#x60; of GET /v1/connect/oauth-apps. | 
**Label** | **string** |  | 
**ClientId** | **string** |  | 
**ClientSecret** | **string** |  | 
**MetaAppId** | **string** | Instagram only: the numeric ID of the Meta app your Instagram app lives in. Zernio uses it with &#x60;metaAppSecret&#x60; to register the webhook. Send both or neither. | [optional] 
**MetaAppSecret** | **string** | Instagram only: the secret of that Meta app. Never returned. | [optional] 
**SlackSigningSecret** | **string** | Slack only: the signing secret from the app&#39;s Basic Information page. Needed to receive events from your Slack app; any other platform is a 400. | [optional] 
**ScopeAreas** | **List&lt;CreateOAuthAppRequest.ScopeAreasEnum&gt;** | Areas this app requests. Defaults to every area the platform supports; an area the platform cannot request separately is a 400. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

