# Zernio.Model.AdKeywordMetrics
Trailing 30-day window. Null on rows synced before the metrics columns existed (re-synced on the keyword's next weekly sweep).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**WindowDays** | **int** |  | [optional] 
**Clicks** | **int** |  | [optional] 
**Impressions** | **int** |  | [optional] 
**Cost** | **decimal** | Account currency, not USD-normalized | [optional] 
**Conversions** | **decimal** |  | [optional] 
**FirstPageCpc** | **decimal?** | Account currency | [optional] 
**FirstPositionCpc** | **decimal?** | Account currency | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

