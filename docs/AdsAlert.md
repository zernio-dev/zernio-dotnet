# Zernio.Model.AdsAlert

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable for the same problem on the same entity. Pass it to POST /v1/ads/alerts/{alertId}/dismiss. | [optional] 
**Kind** | **string** |  | [optional] 
**Severity** | **string** |  | [optional] 
**Title** | **string** |  | [optional] 
**Message** | **string** | What happened, in plain words. For a rejection or delivery issue, the platform&#39;s own reason when it gave one. | [optional] 
**Platform** | **string** |  | [optional] 
**PlatformAdAccountId** | **string** |  | [optional] 
**Entity** | [**AdsAlertEntity**](AdsAlertEntity.md) |  | [optional] 
**AdId** | **string** | The Zernio ad id when the entity is an ad, for GET /v1/ads/{adId}. | [optional] 
**AccountId** | **string** | The Zernio ads connection, on connection_lost and sync_failing alerts. | [optional] 
**Currency** | **string** |  | [optional] 
**DetectedAt** | **DateTime** |  | [optional] 
**Fix** | [**AdsAlertFix**](AdsAlertFix.md) |  | [optional] 
**Dismissed** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

