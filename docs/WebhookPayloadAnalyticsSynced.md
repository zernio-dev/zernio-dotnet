# Zernio.Model.WebhookPayloadAnalyticsSynced
Webhook payload for `analytics.synced`. Fired once per connected account each time its analytics sync cycle completes successfully. Poll-driven (roughly hourly per account), not real-time, and never fired for a skipped or failed cycle.  A TRIGGER, not a transport: it deliberately carries no metrics and no cursor. When it arrives, call `GET /v1/analytics/delta` with YOUR OWN last `nextCursor` to read what changed, across every account, in one paginated stream.  The absent cursor is deliberate. The feed's ordering position is assigned inside the analytics store when the row is materialized, which normally has not happened yet at the moment this event fires, so a cursor minted here could sit ahead of the very rows the event announces and make you skip them. Your own `nextCursor` is always in the feed's own ordering and can never do that.  Because of that same lag, a delta read issued the instant this event lands can legitimately come back empty. That is not \"nothing changed\": poll again with the same cursor you just used rather than treating the account as done.  Subscribe to this event on a DEDICATED webhook endpoint. It is high volume (roughly one delivery per connected account per hour) and a subscription's consecutive-failure count is shared across all of its events, so an outage while this event is flowing can suppress the low-volume publishing events that share the same subscription. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID | 
**Event** | **string** |  | 
**Account** | [**WebhookPayloadAnalyticsSyncedAccount**](WebhookPayloadAnalyticsSyncedAccount.md) |  | 
**Sync** | [**WebhookPayloadAnalyticsSyncedSync**](WebhookPayloadAnalyticsSyncedSync.md) |  | 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

