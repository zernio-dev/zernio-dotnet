# Zernio.Model.PostMetricSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SyncedAt** | **string** | When Zernio read the numbers from the platform. | 
**Views** | **decimal** |  | 
**Likes** | **decimal** |  | 
**Comments** | **decimal** |  | 
**Shares** | **decimal?** | null on platforms that do not return the counter, unlike a real 0. | 
**Saves** | **decimal?** | null on platforms that do not return the counter, unlike a real 0. | 
**WatchSeconds** | **decimal?** | Average watch time; null when the platform gives no watch signal. | 
**CompletionRate** | **decimal?** | null when the platform gives no watch signal. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

