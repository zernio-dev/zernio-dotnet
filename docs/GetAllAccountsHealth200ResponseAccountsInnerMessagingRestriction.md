# Zernio.Model.GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction
Observed from Meta's own error subcodes on our own sends (2534122, 1893063, 2534029), not a live probe. Set on the first refused send and cleared when a later send succeeds, so it lags reality by one send in each direction.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subcode** | **int** |  | [optional] 
**Message** | **string** |  | [optional] 
**FirstSeenAt** | **DateTime** |  | [optional] 
**LastSeenAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

