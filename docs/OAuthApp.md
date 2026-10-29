# Zernio.Model.OAuthApp

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Pass it as &#x60;oauthAppId&#x60; on GET /v1/connect/{platform} to connect through this app. | 
**Platform** | **string** | The platform the app belongs to, as in GET /v1/connect/{platform}. | 
**Label** | **string** |  | 
**ClientId** | **string** | The client ID (or app ID) of your app on the platform. The secret is never returned. | 
**ScopeAreas** | **List&lt;OAuthApp.ScopeAreasEnum&gt;** | The permission areas every connect through this app requests. Pick only what your app is approved for on the platform. | 
**Status** | **string** | &#x60;ok&#x60;: the platform accepted the keys at the last check. &#x60;unchecked&#x60;: the check could not reach a verdict (see lastError). &#x60;invalid&#x60;: the platform rejected the keys; connects and token refreshes through this app will fail until the secret is rotated. | 
**LastCheckedAt** | **DateTime?** |  | [optional] 
**LastError** | **string** |  | [optional] 
**AccountCount** | **int** | Connected accounts currently running on this app. | 
**RedirectUri** | **string** | The OAuth redirect URI to allow in your app&#39;s settings on the platform. | 
**Webhook** | [**OAuthAppWebhook**](OAuthAppWebhook.md) |  | [optional] 
**SharedWebhookUrl** | **string** | TikTok only: set this as the webhook callback URL in your TikTok developer app. TikTok uses it to report when a video finishes publishing; Zernio also checks the publish status itself, so posting works without it. Null on other platforms. | [optional] 
**HasSlackSigningSecret** | **bool** | Slack only: whether the signing secret of your Slack app is saved. Without it Zernio refuses every event sent to &#x60;slackEvents.requestUrl&#x60;. | [optional] 
**SlackEvents** | [**OAuthAppSlackEvents**](OAuthAppSlackEvents.md) |  | [optional] 
**CreatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

