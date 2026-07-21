# Zernio.Model.RfPrediction
A Meta Reach & Frequency prediction. Money values in whole units of the ad account currency.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PredictionId** | **string** |  | [optional] 
**Status** | **string** | ready | pending | failed:&lt;meta code&gt; | [optional] 
**Budget** | **decimal?** | Quoted (or provided) lifetime budget for the window. | [optional] 
**Reach** | **int?** | Predicted (or requested) unique reach. | [optional] 
**Impressions** | **int?** |  | [optional] 
**MinBudget** | **decimal?** | Meta&#39;s allowed lower bound for this spec. | [optional] 
**MaxBudget** | **decimal?** |  | [optional] 
**MinReach** | **int?** |  | [optional] 
**MaxReach** | **int?** |  | [optional] 
**FrequencyCap** | **int?** |  | [optional] 
**StartTime** | **int?** | Unix seconds; the reserved window the R&amp;F ad set will run on. | [optional] 
**StopTime** | **int?** |  | [optional] 
**ExpiresAt** | **string** | When the reservation&#39;s locked price expires (set after reserving). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

