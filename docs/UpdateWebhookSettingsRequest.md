# Zernio.Model.UpdateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Webhook ID to update (required) | 
**Name** | **string** | Webhook name (1-50 characters). Must be non-empty if provided. | [optional] 
**Url** | **string** | Webhook endpoint URL (must be a valid URL, whitespace trimmed). Must be a valid URL if provided. | [optional] 
**Secret** | **string** | Secret key for HMAC-SHA256 signature verification | [optional] 
**Events** | **List&lt;UpdateWebhookSettingsRequest.EventsEnum&gt;** | Events to subscribe to. Must contain at least one event if provided. | [optional] 
**IsActive** | **bool** | Enable or disable webhook delivery | [optional] 
**CustomHeaders** | **Dictionary&lt;string, string&gt;** | Custom headers to include in webhook requests | [optional] 
**DisabledResourceGroups** | **List&lt;UpdateWebhookSettingsRequest.DisabledResourceGroupsEnum&gt;** | Replaces the subscription&#39;s denylist. Send an empty array to clear it and receive every event in &#x60;events&#x60; again. Omitting the field leaves the current denylist untouched. Applies to events emitted after the update; already-queued events can still deliver for up to five minutes after they were enqueued. When the caller is a restricted (zrk_) key, that key&#39;s own disabled groups are unioned back in either way, so a restricted key can neither clear nor widen a subscription past its own groups. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

