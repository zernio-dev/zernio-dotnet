# Zernio.Model.GetSmsUsage200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Since** | **DateTime** |  | [optional] 
**Until** | **DateTime** |  | [optional] 
**GroupBy** | **string** |  | [optional] 
**Profile** | [**UsageProfileRef**](UsageProfileRef.md) | Present with &#x60;profileId&#x60; / &#x60;externalId&#x60;: the profile the counts are scoped to. | [optional] 
**Totals** | [**GetSmsUsage200ResponseTotals**](GetSmsUsage200ResponseTotals.md) |  | [optional] 
**Groups** | [**List&lt;GetSmsUsage200ResponseGroupsInner&gt;**](GetSmsUsage200ResponseGroupsInner.md) | Present (possibly empty) when &#x60;groupBy&#x60; is set. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

