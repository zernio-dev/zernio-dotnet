# Zernio.Model.MetricDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Description** | **string** |  | 
**Unit** | **string** | ratio is a plain ratio (0 to 1 for a rate); money is in the account currency, or the unit and currency meta.units gives; position is a rank where 1 is the top; score runs from 0 to 100. | 
**Additive** | **bool** |  | 
**Source** | **string** | stored: read from what Zernio synced; live: read from the platform on each request. | 
**Platforms** | **List&lt;string&gt;** |  | 
**Freshness** | **string** |  | 
**Granularities** | **List&lt;MetricDefinition.GranularitiesEnum&gt;** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

