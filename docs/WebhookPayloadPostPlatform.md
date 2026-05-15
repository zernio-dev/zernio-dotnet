# Zernio.Model.WebhookPayloadPostPlatform
Webhook payload for the per-platform terminal events `post.platform.published` and `post.platform.failed`. Fires once per platform target inside a post as that platform reaches a terminal state (published or permanent failure). The `post` envelope mirrors the shape of `WebhookPayloadPost` so consumers can reuse rendering logic; the `platform` block identifies which specific platform transitioned; the `account` block identifies the connected social account behind that platform-write. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID. | 
**Event** | **string** |  | 
**Post** | [**WebhookPayloadPostPlatformPost**](WebhookPayloadPostPlatformPost.md) |  | 
**Platform** | [**WebhookPayloadPostPlatformPlatform**](WebhookPayloadPostPlatformPlatform.md) |  | 
**Account** | [**WebhookPayloadPostPlatformAccount**](WebhookPayloadPostPlatformAccount.md) |  | 
**Timestamp** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

