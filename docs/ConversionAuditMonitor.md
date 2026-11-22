# Zernio.Model.ConversionAuditMonitor

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The monitor id. | 
**Host** | **string** | The watched host, lowercase and without &#x60;www.&#x60;. | 
**ReportUrl** | **string** | The host&#39;s public report on is-bleeding.com. | 
**Score** | **int?** | The score of the last check (0 to 100), or null before the first readable scan. | 
**Grade** | **string** | The grade of the last check. | 
**ScoreHistory** | [**List&lt;ConversionAuditMonitorScoreHistoryInner&gt;**](ConversionAuditMonitorScoreHistoryInner.md) | The score of each of the last 30 checks, oldest first. | 
**CreatedAt** | **DateTime** |  | 
**LastCheckedAt** | **DateTime?** |  | 
**NextCheckAt** | **DateTime** | When the next daily check is due. | 
**LastAlertedAt** | **DateTime?** | When the last alert email went out. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

