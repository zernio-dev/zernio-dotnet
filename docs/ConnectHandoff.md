# Zernio.Model.ConnectHandoff

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | [optional] 
**Status** | **string** |  | [optional] 
**Platform** | **string** |  | [optional] 
**Accounts** | [**List&lt;ConnectHandoffAccountsInner&gt;**](ConnectHandoffAccountsInner.md) | Filled when &#x60;status&#x60; is &#x60;connected&#x60;: every account the connect added (several when the user picked several pages, locations or organizations), each checked to be on the profile the connect was started for and written during this handoff. Empty otherwise. | [optional] 
**Error** | [**ConnectHandoffError**](ConnectHandoffError.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

