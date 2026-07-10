# Zernio.Model.ListAdAccounts200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Platform ad account ID (e.g. act_123) | [optional] 
**Name** | **string** |  | [optional] 
**Currency** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**TimezoneName** | **string** | IANA timezone of the ad account (Meta only). Drives daily-budget reset and Insights day boundaries. | [optional] 
**TimezoneOffsetHoursUtc** | **decimal** | Signed UTC offset in hours, reflecting current DST (Meta only). | [optional] 
**Selectable** | **bool** | Meta only. Whether the account can create/run ads now. Absent (treat as true) on non-Meta platforms. | [optional] 
**UnusableReason** | **string** | Meta only. Human-readable reason when selectable is false; null when selectable. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

