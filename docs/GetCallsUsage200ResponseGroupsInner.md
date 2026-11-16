# Zernio.Model.GetCallsUsage200ResponseGroupsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** | The group key: a &#x60;YYYY-MM-DD&#x60; UTC day, one of your numbers, a channel, or a profile id. | [optional] 
**ProfileId** | **string** | With &#x60;groupBy&#x3D;profile&#x60; only: the profile id (same as &#x60;key&#x60;). | [optional] 
**ExternalId** | **string** | With &#x60;groupBy&#x3D;profile&#x60; only: the externalId set on the profile, null when it has none. | [optional] 
**Calls** | **int** |  | [optional] 
**Answered** | **int** |  | [optional] 
**Minutes** | **decimal** |  | [optional] 
**BillableUSD** | **decimal** |  | [optional] 
**MetaUSD** | **decimal** |  | [optional] 
**BrandedCalls** | **int** |  | [optional] 
**BrandedCallUSD** | **decimal** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

