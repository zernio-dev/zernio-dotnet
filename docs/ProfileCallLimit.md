# Zernio.Model.ProfileCallLimit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Limit** | **decimal?** | The limit, or null when none is set at this level. | 
**Used** | **decimal** | Used in the current window, calls still in progress included. | 
**Remaining** | **decimal?** | What is left before the limit; null when there is no limit. | 
**Window** | **string** | &#x60;concurrent&#x60; counts calls in progress now; the rolling windows end now. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

