# Zernio.Model.PostSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SyncedAt** | **DateTime** | When Zernio fetched this reading from the platform | 
**Views** | **int** |  | 
**Likes** | **int** |  | 
**Comments** | **int** |  | 
**Shares** | **int?** | Null on platforms that do not return shares | 
**Saves** | **int?** | Null on platforms that do not return saves | 
**WatchSeconds** | **decimal?** | Average watch time in seconds. Null when the platform gives none. | 
**CompletionRate** | **decimal?** | Share of viewers who watched to the end, 0 to 1. Null when the platform gives none. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

