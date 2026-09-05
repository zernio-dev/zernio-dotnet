# Zernio.Model.Webhook
Individual webhook configuration for receiving real-time notifications

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique webhook identifier | [optional] 
**Name** | **string** | Webhook name (for identification) | [optional] 
**Url** | **string** | Webhook endpoint URL | [optional] 
**Secret** | **string** | Secret key for HMAC-SHA256 signature verification. | [optional] 
**Events** | **List&lt;Webhook.EventsEnum&gt;** | Events subscribed to | [optional] 
**IsActive** | **bool** | Whether webhook delivery is enabled | [optional] 
**LastFiredAt** | **DateTime** | Timestamp of last successful webhook delivery | [optional] 
**FailureCount** | **int** | Consecutive terminal delivery failures (resets to 0 on any successful delivery). Auto-disable only triggers when the endpoint has had no successful delivery within a 3-day window AND either reaches 20 consecutive terminal failures or has been failing continuously for 3 days; any success within that window keeps the endpoint enabled regardless of the count. | [optional] 
**CustomHeaders** | **Dictionary&lt;string, string&gt;** | Custom headers included in webhook requests | [optional] 
**DisabledResourceGroups** | **List&lt;Webhook.DisabledResourceGroupsEnum&gt;** | Resource groups this subscription does not receive (opt-out denylist, same vocabulary and same semantics as the field on API keys). Absent or empty means the subscription receives every event listed in &#x60;events&#x60;, which is how every subscription created before this field existed behaves. An event whose group is listed here is dropped before delivery even when it is still present in &#x60;events&#x60;, and the same check runs on every replay path (test fire, redelivery, dead-letter requeue). Editing the denylist applies to every event emitted afterwards; events already queued when the edit landed can still be delivered for up to five minutes after they were enqueued. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

