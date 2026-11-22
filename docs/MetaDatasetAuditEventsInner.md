# Zernio.Model.MetaDatasetAuditEventsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Last7Days** | **int** |  | 
**Last24Hours** | **int** |  | 
**LastSeenHour** | **DateTime?** | Start of the last hour Meta counted the event in: Meta&#39;s stats are hourly. | 
**Daily** | [**List&lt;MetaDatasetAuditEventsInnerDailyInner&gt;**](MetaDatasetAuditEventsInnerDailyInner.md) |  | 
**ServerSharePct** | **decimal?** | Percent of the window&#39;s events received through the Conversions API. Null when not measured (only the 12 busiest events are split by source). | 
**MatchQuality** | **decimal?** | Event Match Quality, 0 to 10. Meta rates 6 and above as good. | 
**MatchKeys** | [**List&lt;MetaDatasetAuditEventsInnerMatchKeysInner&gt;**](MetaDatasetAuditEventsInnerMatchKeysInner.md) |  | 
**Diagnostics** | [**List&lt;MetaDatasetAuditEventsInnerDiagnosticsInner&gt;**](MetaDatasetAuditEventsInnerDiagnosticsInner.md) |  | 
**Dedup** | [**List&lt;MetaDatasetAuditEventsInnerDedupInner&gt;**](MetaDatasetAuditEventsInnerDedupInner.md) | Per deduplication key, the share of browser and server copies carrying it and of browser copies Meta paired through it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

