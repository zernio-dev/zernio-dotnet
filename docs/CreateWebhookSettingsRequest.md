# Zernio.Model.CreateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Webhook name (1-50 characters) | 
**Url** | **string** | Webhook endpoint URL (must be a valid URL, whitespace trimmed) | 
**Secret** | **string** | Secret key for HMAC-SHA256 signature verification | [optional] 
**Events** | **List&lt;CreateWebhookSettingsRequest.EventsEnum&gt;** | Events to subscribe to (at least one required) | 
**IsActive** | **bool** | Enable or disable webhook delivery. Defaults to &#x60;true&#x60; when omitted. | [optional] [default to true]
**CustomHeaders** | **Dictionary&lt;string, string&gt;** | Custom headers to include in webhook requests | [optional] 
**DisabledResourceGroups** | **List&lt;CreateWebhookSettingsRequest.DisabledResourceGroupsEnum&gt;** | Resource groups this subscription does not receive (opt-out denylist). Omit or send an empty array to receive every event in &#x60;events&#x60;. Listing a group here drops its events before delivery and on every replay path. Set at creation it applies to everything this subscription ever receives; changed later via PUT it applies to events emitted after the change, with a five-minute tail for events already queued (see that operation). When the caller is a restricted (zrk_) key, that key&#39;s own disabled groups are unioned into whatever you send here, so a restricted key can never create a subscription wider than itself. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

